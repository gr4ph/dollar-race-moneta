# Platform facts

Each fact has a source and the date it was checked. **UNVERIFIED** means we haven't confirmed it from an official source yet.

## Shop setup (confirmed by Shaky's screenshots, 2026-10-27)
- Shop listing currency: **USD**.
- Payouts: **MXN** to a Mexican bank via the Etsy Payment account.
- Currency conversion: **2.5%** on top of the market rate, because the listing currency differs from the bank currency.
- RFC: **not on file** in Etsy's tax settings.

## Etsy fees and withholding for a Mexico-based seller
| Item | Rate | Source | Checked |
|---|---|---|---|
| Listing fee | $0.20 per listing (and per auto-renewal when an item sells) | Etsy fee policy | general knowledge, recheck |
| Transaction fee | 6.5% of the order total | [Etsy help 115015628847](https://help.etsy.com/hc/articles/115015628847) (mentions the 6.5%) | 2026-10-27 |
| Payment processing (Mexican bank) | **4.5% + MXN 8** per order | [Etsy help 115015628847](https://help.etsy.com/hc/articles/115015628847) | 2026-10-27 |
| Currency conversion | 2.5% | Shop Manager → Currency screen | 2026-10-27 |
| Offsite Ads | 15% of an order that comes from an offsite ad | general knowledge, recheck | — |
| IVA on Etsy's own fees | **UNVERIFIED**; assumed 16% | — | — |
| ISR withheld, valid RFC | 2.5% (individuals and legal entities; was 1% for individuals before 2026-01-01) | [Etsy help 8709142835223](https://help.etsy.com/hc/articles/8709142835223) | 2026-10-27 |
| ISR withheld, **no RFC** | **20%** | same | 2026-10-27 |
| IVA withheld, valid RFC | 8% on sales to buyers **in Mexico** | same | 2026-10-27 |
| IVA withheld, no RFC | 16% on sales to buyers in Mexico | same | 2026-10-27 |
| IVA on sales to buyers outside Mexico (e.g., US) | **0%** | same | 2026-10-27 |

Notes:
- The processing fee is charged on the full order total, including sales tax.
- With an RFC on file, Etsy issues a CFDI for the taxes it withholds and pays to the SAT.

Net-per-sale estimates and the price floor are in `PLAYBOOK-moneta.md` §7.

## Etsy access from this environment
- Etsy shop and search pages return **HTTP 403** to the team's fetches, so we can't look at the shop or search results directly.
- The Etsy Open API (`openapi.etsy.com/v3`) **is reachable** and asks for an `x-api-key` in the format `keystring:shared_secret`. We store it as the environment variable `ETSY_API_KEY`.

## AI disclosure (Etsy)
- Etsy's House Rules say the listing description must disclose when AI was used to create an item. [Etsy House Rules](https://www.etsy.com/ca/new-guidelines), checked 2026-10-24.

## Canva licensing (secondary sources, recheck against Canva's licence)
- Designs made from free elements may be sold as templates.
- Designs with Pro elements may only be sold as template links, and buyers without Pro may see watermarks. That's why we use **free elements only**.
- Reselling Canva's own templates, or barely changed copies of them, is not allowed.
- Source: [FitSmallBusiness](https://fitsmallbusiness.com/how-to-sell-canva-templates-on-etsy/), checked 2026-10-24.
