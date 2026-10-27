# Platform facts

Each fact has a source and the date it was checked. **UNVERIFIED** means we haven't confirmed it from an official source yet.

## Shop setup (confirmed by Shaky's screenshots, 2026-10-27)
- Shop listing currency: **USD**.
- Payouts: **MXN** to a Mexican bank via the Etsy Payment account.
- Currency conversion: **2.5%** on top of the market rate, because the listing currency differs from the bank currency.
- RFC: **not on file** in Etsy's tax settings. Shaky's accountant says to keep it that way for now, so price for the 20% ISR withholding.
- The 20% is sent to the SAT; Etsy doesn't release it later. Whether it can be credited or counts as a final payment (Mexican sources cite LISR art. 113-B) is for Shaky's accountant. Sources: [El Contribuyente](https://www.elcontribuyente.mx/2024/06/personas-fisicas-sin-rfc-que-operan-en-plataformas-pagan-mas-impuestos/), [Siigo](https://www.siigo.com/mx/blog/obligaciones-fiscales/regimen-plataformas-digitales-sat-obligaciones/). Checked 2026-10-27.

## Etsy fees and withholding for a Mexico-based seller
| Item | Rate | Source | Checked |
|---|---|---|---|
| Listing fee | $0.20 per listing (and per auto-renewal when an item sells) | Etsy fee policy | general knowledge, recheck |
| Transaction fee | 6.5% of the order total | [Etsy help 115015628847](https://help.etsy.com/hc/articles/115015628847) (mentions the 6.5%) | 2026-10-27 |
| Payment processing (Mexican bank) | **4.5% + MXN 8** per order | [Etsy help 115015628847](https://help.etsy.com/hc/articles/115015628847) | 2026-10-27 |
| Currency conversion | 2.5% | Shop Manager → Currency screen | 2026-10-27 |
| Offsite Ads | 15% of an order that comes from an offsite ad (12% once a shop has made $10k in 365 days); capped at $100 per order. Shops that have never made $10k can opt out | [Etsy help 360000338367](https://help.etsy.com/hc/articles/360000338367) | 2026-10-27 |
| IVA on Etsy's own fees | **Charged** for Mexico shops (confirmed). The rate isn't stated; assumed **16%** (UNVERIFIED, check the first monthly statement) | [Etsy help 360040584433](https://help.etsy.com/hc/en-us/articles/360040584433-How-VAT-Is-Collected-on-Seller-Fees) | 2026-10-27 |
| ISR withheld, valid RFC | 2.5% (individuals and legal entities; was 1% for individuals before 2026-01-01) | [Etsy help 8709142835223](https://help.etsy.com/hc/articles/8709142835223) | 2026-10-27 |
| ISR withheld, **no RFC** | **20%** | same | 2026-10-27 |
| IVA withheld, valid RFC | 8% on sales to buyers **in Mexico** | same | 2026-10-27 |
| IVA withheld, no RFC | 16% on sales to buyers in Mexico | same | 2026-10-27 |
| IVA on sales to buyers outside Mexico (e.g., US) | **0%** | same | 2026-10-27 |

Notes:
- The processing fee is charged on the full order total, including sales tax.
- With an RFC on file, Etsy issues a CFDI for the taxes it withholds and pays to the SAT.

- Exchange rate: about 1 USD = 18.59 MXN (third-party rate, 2026-10-27), so MXN 8 ≈ $0.43.

Net-per-sale estimates and the price floor are in `PLAYBOOK-moneta.md` §7.

## Etsy access from this environment
- Etsy shop and search pages return **HTTP 403** to the team's fetches, so we can't look at the shop or search results directly.
- The Etsy Open API (`openapi.etsy.com/v3`) **is reachable** and asks for an `x-api-key` in the format `keystring:shared_secret`. The key is stored as a **network secret** in the cloud environment (header `x-api-key`, allowed host `openapi.etsy.com`). It's added to our requests automatically, so scripts never read or send it themselves.

## AI disclosure (Etsy)
- Etsy's House Rules say the listing description must disclose when AI was used to create an item. [Etsy House Rules](https://www.etsy.com/ca/new-guidelines), checked 2026-10-24.

## Canva licensing (secondary sources, recheck against Canva's licence)
- Designs made from free elements may be sold as templates.
- Designs with Pro elements may only be sold as template links, and buyers without Pro may see watermarks. That's why we use **free elements only**.
- Reselling Canva's own templates, or barely changed copies of them, is not allowed.
- Source: [FitSmallBusiness](https://fitsmallbusiness.com/how-to-sell-canva-templates-on-etsy/), checked 2026-10-24.

## Digital listings (confirmed, help.etsy.com, 2026-10-27)
- Up to **5 files per listing, 20 MB each**. PDF, PNG, JPG and ZIP are allowed. A Canva template is delivered as a PDF containing the link.
- Return or exchange policies **can't be set on digital listings**. Problems are handled case by case, and Etsy's purchase protection may still apply.
- Sources: [add files](https://help.etsy.com/hc/en-us/articles/115015628347), [return policies](https://help.etsy.com/hc/en-us/articles/7869401615255).

## Etsy rules on AI and bots (confirmed: help.etsy.com "What Can I Sell on Etsy?")
- Disclose AI use in the listing description.
- **Banned:** bot-generated content, AI-generated functional instructions (recipes, craft patterns, guides) and AI prompt bundles.
- Digital items must be made or designed by the seller.
- Reported by third parties only (UNVERIFIED): an Oct 22, 2026 update removes fully bot-generated listings and expects a visual preview of what the buyer receives.
- **For us:** no recipe, pattern or guide products. Every listing shows real previews. **Shaky reviews each listing before it's published.**

## Etsy Open API v3 (confirmed on help.etsy.com and developers.etsy.com, 2026-10-27)
- **Seller app:** for your own shop only, usually approved **within minutes**. Use this one, not a "personal app", which goes through a longer review.
- Every request needs the `x-api-key` header. Writes and private data also need OAuth 2.0 with PKCE (scopes `listings_r` and `listings_w`).
- **Draft flow:** `createDraftListing` → `updateListing` with type="download" → `uploadListingFile` → `uploadListingImage`. Only Shaky activates a listing.
- **Tested 2026-10-27 (CONFIRMED):** the network secret works. `openapi-ping`, `getShop` and keyword search (`GET /v3/application/listings/active?keywords=…`) all return HTTP 200 with the seller app key alone. Search returns a `count` of matching active listings. Example: "dog groomer gift certificate" = 53, "gift certificate template" = 31,311.
- Our shop (via API): shop_id 43900445, created May 2023, 0 active listings, 0 sales, 0 reviews, 0 favorites, not on vacation, currency USD, no title or announcement set.
- **API Terms of Use** (full text pasted by Shaky, 2026-10-27). They contain **no AI clause**. The points that matter for us:
  - **§9: no scraping.** Bots may not read or analyze the Etsy website; the API is the only allowed programmatic route. We don't fetch etsy.com pages (shop, listing, search or help) with tools.
  - **§1:** cache or store Etsy content only for reasonable periods. Never store other members' personal data. Respect sellers' rights to their own content. Be truthful about the app. Stay under 10,000 calls a day.
  - **§4:** managing your own shop is a reasonable commercial use. Don't resell API data or access.
  - **§2:** don't use Etsy's marks in a way that suggests endorsement. The app name "Moneta Shop Tools" doesn't use them.
- Sources: [register a seller app](https://help.etsy.com/hc/en-us/articles/41918478450967), [listings tutorial](https://developers.etsy.com/documentation/tutorials/listings).

Full researcher notes: `research/verification-notes.md`.
