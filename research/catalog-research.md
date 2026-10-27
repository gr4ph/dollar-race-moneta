# Catalog research (Team Moneta, Researcher) - checked 2026-10-27

Legend: **CONFIRMED** = read on an official page I could open. **UNVERIFIED** = third-party source, search snippet, my own calendar arithmetic, or an official page I could not open. Etsy shop/search pages and canva.com template pages return HTTP 403 to fetch, so every Etsy and Canva number below came from web-search result summaries (review and sales counts as displayed on listings, not audited).

---

## 1. Etsy shop rename rules

Official sources: [How to Change Your Shop Name](https://help.etsy.com/hc/en-us/articles/115015710568-How-to-Change-Your-Shop-Name) (fetched), [What's the Link for My Shop?](https://help.etsy.com/hc/en-us/articles/360000338087-What-s-the-Link-for-My-Shop) (fetched), [How to Open an Etsy Shop](https://help.etsy.com/hc/en-us/articles/115015672808-How-to-Open-an-Etsy-Shop) (fetched), [How your Username, Shop Name, and Preferred Name Represent You](https://help.etsy.com/hc/en-us/articles/360000337387-How-your-Username-Shop-Name-and-Preferred-Name-Represent-You) (fetched).

| Question | Answer | Status |
|---|---|---|
| How to change it | Shop Manager -> Settings -> Your shop -> under "Shop name" select Edit -> enter new name -> save. (After opening, also under Info & Appearance -> Shop Name tab.) | CONFIRMED |
| How many times | After the shop is open: up to **5 changes** on your own. After 5, each change needs approval from Etsy Support. Capitalization-only edits and going back to a previous name do **not** count. Before opening: unlimited. | CONFIRMED |
| Length | Up to **20 characters** (rename article). The "open a shop" article says **4 to 20**. | CONFIRMED |
| Characters | **No spaces, no punctuation or special characters.** Capital letters inside the name ("ShopName") are the suggested way to separate words. No profanity. | CONFIRMED |
| Uniqueness | Name must not belong to another member. A name used by any open shop can't be reused even if that shop is later closed. A name used on another account can't be reused even if that account is closed. Your old name is reserved: other sellers can't take it. | CONFIRMED |
| Trademarks | The name can't infringe someone else's trademark (our rule 7 also applies). | CONFIRMED |
| URL / subdomain | Shop URL updates automatically: `shopname.etsy.com` and `etsy.com/shop/shopname`. Links with the old name **automatically redirect** to the new one. | CONFIRMED |
| 45-day marker | For 45 days an icon next to the shop name (shop page, profile, search results) tells shoppers the name changed. It does not block further changes. | CONFIRMED |
| Reviews and sales history | **The help articles say nothing about it.** Third-party guides say reviews, sales history and favorites stay because it is the same shop and account; no Etsy statement found. | **UNVERIFIED** (likely true) |
| Username | Unchanged. You can't sign in with the shop name if it differs from the username. | CONFIRMED |
| Not covered by Etsy | How long the redirect lasts; whether section links (`section_id=`) and keyword links (`search_query=`) redirect; whether an own-domain redirect still works; any search-ranking effect of renaming. | **UNVERIFIED** |
| Waiting period between changes | None described. | CONFIRMED (absence) |

Practical points for the manager:
- Update logo, banner, announcement, About section and listing footers ("shop name in PDF footer", PLAYBOOK section 4) after renaming; the old name is also baked into any PDFs already delivered.
- Pick the new name once. Five free changes exist but each change resets the 45-day "changed" icon (inference).
- A trademark pre-check of the candidate name (e.g. a search on uspto.gov) is outside what Etsy's help pages promise; Etsy only says the name can't infringe.

---

## 2. Checking for an existing Etsy developer app

- **Page:** `https://www.etsy.com/developers/your-apps` ("Your Apps"; also reachable from the Developer Portal, `https://www.etsy.com/developers`, signed in with the shop owner's Etsy account). CONFIRMED by Etsy's [Authentication guide](https://developers.etsy.com/documentation/essentials/authentication): "You can find both values on the Your Apps page."
- **What it shows (CONFIRMED):** each registered app with its **API keystring** and **shared secret** (the `x-api-key` header is `keystring:shared_secret`), and it lets you edit the app's redirect URIs. Third parties say a "See API Key Details" dropdown on that page shows a **Status** field (pending or approved): UNVERIFIED. Etsy's docs do not name status labels.
- **More than one app?** Not stated by Etsy. The [seller-app registration article](https://help.etsy.com/hc/en-us/articles/41918478450967-How-to-Register-a-Seller-App-with-Etsy-s-API) lists as an eligibility condition "Do not already have a registered app" (the developer docs word it "doesn't already have an active app"). So an existing app **blocks creating a new seller app**. Whether personal apps allow several: not stated, UNVERIFIED.
- **If an old app exists:** (1) open Your Apps and read its keystring and status; (2) if it is approved, reuse it: Shaky puts `keystring:shared_secret` into the cloud environment as `ETSY_API_KEY`, never in chat or the repo; (3) check it is a seller app for this shop, and add the OAuth redirect URI we need; (4) if it is stuck pending or rejected, Etsy publishes no step for it, so the only route found is a third-party one, emailing developer@etsy.com (UNVERIFIED).
- **Don't confuse with:** Shop Manager -> Apps -> **Connected apps** tab. That lists third-party apps connected to the shop (the old print-on-demand integration may show up there and can be disconnected). It is not the developer app list ([source](https://help.etsy.com/hc/en-us/articles/360025870013-What-is-Etsy-s-API)).
- Whether renaming the shop affects an existing app or key: not documented, UNVERIFIED.

---

## 3. Seasonal calendar, Nov 2026 to Dec 2027

Dates were computed from fixed rules (Thanksgiving = 4th Thursday of November, Mother's Day = 2nd Sunday of May, Father's Day = 3rd Sunday of June, Labor Day = 1st Monday of September, Memorial Day = last Monday of May) and cross-checked on weekdays (Oct 27, 2026 is a Tuesday). Easter 2027, Hanukkah 2026, Teacher Appreciation Week and tax dates come from the sources named.

**How to read "lead time":** the only hard, official-style numbers I found are National Retail Federation (NRF) consumer surveys. Everything else is an estimate and is marked **EST (UNVERIFIED)**. Business owners who buy templates likely search **2 to 4 weeks earlier** than consumers, because they must publish promotions before the consumer peak (inference, UNVERIFIED). Third-party claims that Etsy ranking lags 3 to 6 weeks after listing are unsourced (UNVERIFIED), but they imply the practical "list by" date is well before the buyer's search date.

NRF evidence used:
- Winter holiday (survey Oct 1-7, 2026, released Oct 20): **43% start before November**, **64% plan to do most shopping Thanksgiving weekend**, gift cards are the **#1 wish-list item at 47%**. [NRF](https://nrf.com/media-center/press-releases/affordability-shapes-winter-holiday-shopping-according-to-nrf-holiday-survey)
- Halloween (survey Sept 1-9, 2026): **49% start in September or earlier**. [NRF](https://nrf.com/media-center/press-releases/nrf-halloween-survey-shows-consumer-spending-expected-to-reach-13-5-billion)
- Back to school (survey July 1-8, 2026): **62% had started by early July**. [NRF](https://nrf.com/media-center/press-releases/majority-of-back-to-school-shoppers-get-a-head-start-on-the-season)
- Mother's Day (survey Apr 1-8, 2026): top gifts flowers 75%, greeting cards 74%, special outings 63%, gift cards 55%; the release gives no timing. [NRF](https://nrf.com/media-center/press-releases/mother-s-day-spending-expected-to-hit-record-38-billion)
- Pinterest (UK data, July 2023-June 2024): calendar moments start about 2 months ahead; Christmas spikes Oct-Nov; Easter planning Feb-Mar; Halloween momentum from September. UK data, may not match US. [ppc.land summary](https://ppc.land/pinterest-reveals-key-marketing-moments-and-search-trends-for-2025/)

| Event | 2026 / 2027 date | When US buyers start searching (lead time) | Product types that fit our formats |
|---|---|---|---|
| Thanksgiving | Thu **Nov 26, 2026**; Thu Nov 25, 2027 | EST (UNVERIFIED): hosts plan 2-4 weeks ahead. Today is 30 days out, so the window is nearly gone for new listings. | Printable: potluck sign-up sheet, hosting-day schedule planner, place cards. Canva: closure/holiday-hours notice for small businesses. No recipes. |
| Post-Thanksgiving shopping weekend (generic terms only) | Fri Nov 27 - Mon Nov 30, 2026; Fri Nov 26 - Mon Nov 29, 2027 | NRF: 64% do most shopping that weekend; 43% start before November. Small businesses prepare promos early-to-mid November (EST, UNVERIFIED). | Canva: "holiday sale" sign and social post set, gift certificate template (shops sell gift cards here). Printable: gift budget tracker. Avoid event brand names (see note below). |
| Christmas / holiday season | Fri **Dec 25, 2026**; Sat Dec 25, 2027. Hanukkah Dec 4-12, 2026 (one university calendar, UNVERIFIED). | NRF: 43% before November. Pinterest UK: Christmas searches spike Oct-Nov. One third-party calendar says Oct 20 - Dec 18 with the highest day volume in the second week of December (no method, UNVERIFIED). For 2027 the safe "list by" is about Sept 1-Oct 1, 2027 (EST). | Canva: trade-specific gift certificates, holiday hours/closure, pre-order form, thank-you inserts. Printable: Christmas card address list, teacher gift list, gift budget tracker, potluck/white-elephant sign-up, kids' holiday travel checklist. |
| New Year 2027 planning | Fri **Jan 1, 2027** (planning Dec 26 - mid-Jan) | Starts right after Christmas; planners are searched from late November (EST, UNVERIFIED). A third-party calendar says "live by late November". | Printable: 2027 planners, goal and habit trackers, budget tracker, content calendar, mileage/expense log. Canva: Q1 promo post set, "new year" gift certificate (trainers, coaches). |
| Valentine's Day | Sun **Feb 14, 2027** | Third-party window about Jan 20 - Feb 10 (that source contradicts itself; UNVERIFIED). EST: list by early January. NRF Jan 2026: greeting cards 41%, "an evening out" 39% of celebrants. | Canva: date-night / spa gift certificates, mini-session price list, sale posts. Printable: classroom card-exchange list, party sign-up, couples' date-night tracker. |
| St. Patrick's Day | Wed **Mar 17, 2027** | EST (UNVERIFIED): 2-4 weeks ahead. Small event; low priority. | Canva: bar/cafe event flyer and sale post. Printable: classroom or party sign-up. No characters. |
| Easter (Good Friday Mar 26) | Sun **Mar 28, 2027** | Pinterest UK: planning intensifies Feb-Mar. Third-party: smaller peak late March, list by early March. Passover 2027: evening Apr 21 - Apr 29 (optional, one source). | Canva: bakery/market pre-order form (layout only), mini-session price list, brunch sale post. Printable: egg-hunt party sign-up, basket/gift tracker. |
| Spring cleaning | No fixed date. Spring equinox about Sat Mar 20, 2027 (UNVERIFIED, not searched). | **No source found** for when searches start; EST March-April (UNVERIFIED). | Printable: cleaning schedule, declutter tracker, room-by-room checklist (blank layout). Canva: cleaning-business price list, intake form, booking card. |
| Tax season (self-employed / small business) | Final 2026 estimated payment **Jan 15, 2027** (IRS); Form 1040 due **Thu Apr 15, 2027** (third party + weekday check); 2027 estimated dates Apr 15, Jun 15, Sep 15 are computed, not yet on an IRS form. [IRS Taxpayer Advocate](https://www.taxpayeradvocate.irs.gov/news/tax-tips/your-tax-to-do-list-important-tax-dates/2026/) | EST (UNVERIFIED): record-keeping searches Dec-April; year-end clean-up in December. | Printable: income/expense log, mileage log, receipt tracker, year-end checklist. Say plainly "not tax advice" (rule 9). |
| Teacher Appreciation Week | Mon-Fri **May 3-7, 2027** (National Teacher Day Tue May 4); one calendar says May 4-8 but its weekday is wrong. | EST (UNVERIFIED): 2-3 weeks ahead. | Canva: generic teacher thank-you card, gift certificate. Printable: class gift contribution tracker. |
| Mother's Day | Sun **May 9, 2027** | Third-party: about 4 weeks ahead (UNVERIFIED). NRF: gift cards are bought by 55% of celebrants, outings 63%. (UK Pinterest "March peak" is UK Mother's Day; ignore for the US.) | Canva: spa, massage, salon, house-cleaning gift certificates; brunch/mini-session price list; sale posts. Printable: brunch sign-up, gift tracker. |
| Graduation | Peak May, smaller in June 2027; no single date (local school calendars: ceremonies roughly May 9 - mid-June in 2026). | Third-party: about 6 weeks before each region's ceremonies (UNVERIFIED). | Printable: graduation-party planner and RSVP tracker, thank-you note tracker, grad gift list. Canva: gift certificate (photographer, tutor), open-house sign. |
| Summer: Memorial Day to July 4 | Mon May 31, 2027; Sun Jul 4, 2027 (observed Mon Jul 5) | EST (UNVERIFIED): 2-3 weeks ahead. | Canva: summer sale post set, seasonal hours. Printable: kids' summer schedule and chore chart, BBQ sign-up. |
| Father's Day | Sun **Jun 20, 2027** | Third-party 2026 window: about May 25 - Jun 18; list by May 1 (UNVERIFIED). | Canva: barber, detailing, gym gift certificates; sale posts. Printable: gift tracker. |
| Wedding season | Peak Sept-Oct (The Knot: October 17% of weddings in 2023, September 15% in 2024); only 23% of weddings fall Nov-Mar. Engagements peak around December per an older report (UNVERIFIED). [The Knot](https://www.theknot.com/content/fall-most-popular-wedding-season) | Couples plan many months ahead (UNVERIFIED); wedding vendors buy business templates in the off-season (inference). | Printable: wedding budget tracker, planning checklist, guest-list tracker. Canva: vendor price list, thank-you insert. Wedding invitations are a crowded category; I'd skip. |
| Back to school | Late July - September 2027; Labor Day **Mon Sept 6, 2027**; district start dates vary (UNVERIFIED). | NRF 2026: 62% had started by early July; 32% in early June. So June-July for 2027. | Printable: homework/assignment tracker, parent school-year planner, class sign-up sheets, kids' routine chart. Canva: tutoring/after-school price list. |
| Fall / Halloween | Sun **Oct 31, 2027** (Thanksgiving Nov 25, 2027) | NRF 2026: 49% start by September; Pinterest UK: momentum from September. List by mid-August (EST). | Canva: pumpkin patch / farm stand price signs, fall market vendor signs, mini-session price list. Printable: party sign-up, trick-or-treat route log. No characters or movie/brand costumes. |

Notes:
- **Event names:** I avoided "Small Business Saturday". "Black Friday" and "Cyber Monday" are common phrases but their trademark status was **not checked** (UNVERIFIED); my earlier keyword list used "black friday" in one row. The Reviewer should decide; "post-Thanksgiving sale" is the safe generic wording.
- **What is still reachable from today (Oct 27, 2026):** New Year 2027, tax-season logs, Valentine's, and wedding/engagement-season items have realistic windows. Thanksgiving is essentially closed. Christmas is tight (about 7 weeks; the ranking-lag claim is unverified).

---

## 4. Evergreen demand

**Honest limit:** no category here has verified sales volume. Signals are (1) Etsy listings and review/sales counts as displayed in search-result summaries (shop-level sales counts are cumulative, not per product), (2) seller-marketing blogs with no stated method, (3) the existence of Etsy market pages. Price levels matter for us: **our floor is $3.99**, and many comparable listings sit at $1 to $3.

### (a) Small-business Canva templates

| # | Category | Demand signal found | Competition / price note | Source |
|---|---|---|---|---|
| 1 | Gift certificate / voucher | NRF: gift cards are the #1 wish-list item (47%), so shops sell them. Many Etsy listings, trade variants (salon, spa, nails). | Listings about $1.50-$14, several $2-$6. Canva offers free gift-certificate templates (result pages up to continuation=900, so hundreds). | [NRF](https://nrf.com/media-center/press-releases/affordability-shapes-winter-holiday-shopping-according-to-nrf-holiday-survey), [Etsy example](https://www.etsy.com/listing/1290470463/gift-certificate-template-canva), [Canva](https://www.canva.com/gift-certificates/templates/) |
| 2 | Price list / service menu | One result shows a shop with 11.5k sales (shop-level) and another listing 4.8 from 331 reviews. First page was near-identical salon/spa designs. | $2-$9, many at the low end. Canva offers free price-list templates. | [Etsy example](https://www.etsy.com/listing/1718108979/editable-price-list-template-canva), [Canva](https://www.canva.com/templates/s/price-list/?continuation=500) |
| 3 | Loyalty / punch card | Many listings and Etsy market pages exist. No sales counts seen. | $1-$10, mostly $2-$5. Canva lists 1,075+ free loyalty-card designs. | [Etsy market](https://www.etsy.com/market/loyalty_punch_cards), [Canva](https://www.canva.com/business-cards/templates/loyalty-card/?continuation=50) |
| 4 | Client intake / onboarding form per trade (non-legal, non-medical) | Many trade-specific listings: cleaning, organizer, virtual assistant, web design, counselor, esthetician. | $2-$8, bundles $6-$9. Trade focus is how sellers differentiate. Skip consent or health forms. | [Etsy example](https://www.etsy.com/listing/1674405664/cleaning-services-client-intake-form), [example](https://www.etsy.com/listing/1454692159/editable-professional-organizer-client) |
| 5 | Invoice / receipt / quote sets | Many listings, sets of 3 common, Etsy market pages exist. | $1-$5, below our floor unless bundled. | [Etsy market](https://www.etsy.com/market/invoice_template), [example](https://www.etsy.com/listing/4322147547/editable-invoice-template-small-business) |
| 6 | Social media post / story sets | Listed first among Canva categories by seller blogs (no sales data, no method). | Claimed $8-$18, crowded. | [Outfy](https://www.outfy.com/blog/top-selling-digital-products-on-etsy/) |
| 7 | Thank-you / order-insert cards for small sellers | Many listings, Etsy market pages exist, audience is other Etsy sellers. | $1-$9. | [Etsy market](https://www.etsy.com/market/thank_you_insert), [example](https://www.etsy.com/listing/1492849910/editable-thank-you-card-template-small) |
| 8 | Branding kits (palette + covers + stationery) | Named by seller blogs; one real-estate bundle at $41.40 shows 1.4k+ reviews (analyst page, bestseller data labelled 2024). | Bundles reach higher prices; real-estate niche is unsuited to us. | [Accio](https://www.accio.com/business/best-selling-canva-templates-etsy-examples) |

Not recommended from the sources: PLR/MRR bundles (resale rights; breaks our rule 7).

### (b) Home and personal printables

| # | Category | Demand signal found | Competition / price note | Source |
|---|---|---|---|---|
| 9 | Cleaning schedule / chore chart | Strongest signal found. Displayed: Editable Family Chore Chart 4.9 from 129 reviews, 78k sales (shop-level count); Weekly Cleaning Schedule Printable shop 4.9k reviews, 42.3k sales; ADHD Cleaning Planner Bundle 4.8, 18.7k sales. | Entrenched shops. Keep layouts blank; a pre-written task list may count as "functional instructions" (UNVERIFIED how Etsy enforces). | [Etsy](https://www.etsy.com/listing/1209838466/editable-family-chore-chart-printable), [Etsy](https://www.etsy.com/listing/948464527/weekly-cleaning-schedule-printable-chore) |
| 10 | Budget planner / tracker | A top PDF budget planner displays 4.8 from 1,722 reviews. | Crowded; some bundles with habit pages. | [Etsy](https://www.etsy.com/listing/664536090/pdf-budget-planner-printable-habit) |
| 11 | Habit tracker | Many Etsy market pages. Most-reviewed monthly tracker about 500 reviews at $2.00. | Typical $1-$3, below our floor, so bundle. | [Etsy market](https://www.etsy.com/market/habit_tracker_printable) |
| 12 | Practical checklists (moving, cleaning, daily care) | Etsy "Top Selling Checklists" page (blocked for us; contents seen through a search summary: cleaning, moving, senior-care daily task tracker). | Utility niches. | [Etsy](https://www.etsy.com/market/top_selling_checklists) |
| 13 | Planners (weekly, goal, ADHD-friendly) | Etsy "Top Selling Printable Planners" page exists; one top listing about 7.3k reviews. Blog claims ADHD-planner search +340% (Q1 2025 to Q1 2026) is **UNVERIFIED**. Generic planners called saturated (unsourced "50,000+ listings"). | Narrow sub-niches advised by blogs, no data. | [Etsy](https://www.etsy.com/market/top_selling_printable_planners), [Sidequest](https://sidequeststack.com/blog/best-digital-products-to-sell-on-etsy-2026.html) |
| 14 | Wedding budget / planning tracker | Analyst page shows a wedding planner spreadsheet at $9.25 with 12.1k+ reviews. Seasonal-evergreen. | Dominated by large shops. | [Accio](https://www.accio.com/business/best-selling-canva-templates-etsy-examples) |

Weak/no signal: pet-care logs and similar sub-niches appear only in blogs with no data ([DraftMill](https://www.draftmill.co/blog/5-low-competition-etsy-niches-for-digital-downloads-2026) states no sources). Booking/appointment cards: no listing found in my search (UNVERIFIED either way).

---

## 5. Positioning signal

**Direct evidence comparing A, B and C for a new shop: none found.** Etsy publishes no such data; third-party advice is unsourced. What follows is what the sources do show.

What Etsy itself says (CONFIRMED, [Search Visibility page](https://help.etsy.com/hc/en-us/articles/25869947521175-How-to-Use-the-Etsy-Search-Visibility-Page) and the help-center summary of ranking): ranking uses listing relevance (titles, tags, attributes), listing quality (photo, most specific category, return policy), and customer experience (reviews, response time). It does **not** mention shop-wide focus, listing age, or a boost for new shops (the page says nothing about them). Etsy's "reviews weigh recent history" change dated March 2026 appeared only in a search summary: UNVERIFIED.

| | Pros (evidence) | Cons (evidence) |
|---|---|---|
| **A. Small-business templates** | Trade-specific variants are how sellers differentiate (intake forms per trade, salon/spa gift certificates). Canva-template price points ($2-$14 seen; our playbook $4.99-$8.99) fit above our $3.99 floor better than trackers do. Demand is not tied to one date (gift cards #1 wish-list item, NRF). | First pages are near-identical and crowded; Canva itself offers hundreds to 1,000+ free templates in the same categories; many listings at $1-$5; buyer needs a Canva account. Q4 gift-certificate peak is already under way. |
| **B. Home and holiday printables** | Largest visible demand: top listings display tens of thousands of sales and thousands of reviews. Many dated peaks each year (see section 3); NRF shows early shoppers (43% before November, Halloween 49% by September). | Visible winners are entrenched shops with thousands of reviews. Common price $1-$3, under our $3.99 floor (bundling needed). Holiday peaks are short and need listing 4+ weeks ahead (third-party). Free printables on Pinterest are cited as the real competitor for generic items. Etsy's AI rule on "functional instructions" makes pre-written checklists a grey area. |
| **C. Both under one brand** | No Etsy source shows shop-wide focus affecting ranking. Third-party claims that focused shops do better (e.g. "50 listings in one niche beats 200 across ten") cite no data. A seasonal printable line can fill gaps between business peaks. | Same unproven blogs say a clear niche helps; a mixed shop has less credibility for a no-review shop (UNVERIFIED claim). The shop name/branding must cover both. |

What the evidence supports, kept to the facts:
1. **New shops are advised to target narrow phrases**, not broad ones, by every third-party source found (none with data). This is the only point where sources agree.
2. **Neither A nor B shows an advantage for a shop with zero reviews.** Etsy lists customer reviews as a ranking input; no source quantifies the effect or time to first sale (searched; nothing found).
3. **Price floor interaction:** A's templates sell at or above $3.99 more often than B's trackers. B's best-reviewed examples sit at $1-$3 or are large bundles.
4. **Weak lean for the manager to weigh (inference, not data):** A led by trade-specific templates, with B seasonal printables as satellites (C with one main line). This is judgment from points 1-3; it is not proven by any source.

Open doubts: (1) review/sales numbers come from search summaries, not audited pages; (2) Shaky can run the 2-minute Etsy search check per phrase for result counts; (3) the Etsy API (once `ETSY_API_KEY` exists) is the only route to real counts, and whether a seller-app key can run `findAllListingsActive` is still UNVERIFIED (see `research/verification-notes.md`).
