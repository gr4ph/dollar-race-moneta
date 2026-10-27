# Team Moneta: Idea Review

_Session 1 brainstorm (2026-10-24). This is the full analysis; the log only summarizes it._

> **Update 2026-10-27:** Shaky changed the focus. This is no longer a 7-day $1 challenge but an ongoing Etsy shop business, using the plan below.
>
> The pricing math below assumed US-style fees and is **superseded**. The shop's bank is in Mexico (processing is 4.5% + MXN 8), Etsy charges a 2.5% currency conversion, and it withholds 20% ISR while no RFC is on file. The new minimum price is **$3.99**; see `PLAYBOOK-moneta.md` §7 and `research/platform-facts.md`.

## Constraints agreed with Shaky

- A sale **counts once it shows in the Etsy shop balance**. Etsy holding part of the money in reserve doesn't matter.
- **$1 means net, after Etsy fees.**
- Shaky pays Etsy listing fees. The **team budget is still $0**, with **no paid ads**.
- **No personal network.** Buyers must be strangers: no friends, followers or contacts.
- **Digital products only, not customizable**, as little friction as possible, and ideally no refunds.
- Shaky's Etsy shop is 3 years old. It was opened for Printify POD and has no current listings.
- Shaky has **Canva Premium**.
- Shaky will reset the deadline once everything is ready.

## Shaky's ideas

### 1. Etsy print on demand (Printify): low confidence, replaced
- **$1 by deadline at $0?** Unlikely. New POD listings get little search traffic in a week. Printify charges the production cost when an order comes in, and fulfillment adds delay.
- **Rules?** OK only with original designs. "Trending" POD designs often copy trademarks, and AI use must be disclosed.
- **Shaky's work:** connect Printify, approve products, upload listings.
- **Confidence:** low. **Verdict:** the same shop is better used for digital downloads (see the recommendation).

### 2. Trading (crypto/forex): rejected
- Trading profit comes from the market, not a customer, so it doesn't meet the mission. It needs capital, which breaks the $0 budget. It's speculative money-at-risk, which goes against rule 4. Expected 7-day returns after fees are zero or negative.
- **Confidence:** none.

### 3. Online betting (sports/casino): rejected
- Rule 4 bans gambling outright. There's no customer and it needs a stake. The house edge means no strategy wins over time, and bonus-hunting breaks bookmaker terms.
- **Confidence:** none.

## Manager's ideas

| ID | Idea | Status | Confidence |
|---|---|---|---|
| **E2** | Etsy niche printables (e.g., hobby trackers, vendor price sheets) | **Picked** (with E3) | medium |
| **E3** | Etsy editable Canva templates for small sellers (e.g., trade-specific holiday gift certificates, craft-fair signs) | **Picked** (with E2) | medium |
| E1 | Etsy broad holiday printables | Folded into E2/E3 as a seasonal angle | low–medium |
| E4 | Etsy personalized digital items (Santa letter, chore chart) | Dropped: Shaky doesn't want customizable products | low–medium |
| E5 | Etsy POD (idea 1) with fees covered | Dropped: slower and riskier than digital | low |
| A | "Agent Team Starter Kit" for Claude Code, pay-what-you-want on Payhip/Ko-fi, launched on r/ClaudeAI, r/SideProject, Indie Hackers | Backup | medium |
| B | Holiday printables kit on Payhip/Ko-fi + Pinterest | Merged into the Etsy plan | low–medium |
| C | 24h micro-service via [OFFER] posts | Dropped: uses too much of Shaky's time | low–medium |

**Ruled out:**
- Fiverr and Upwork: new sellers' money is held past the deadline.
- Redbubble, TeePublic, KDP and Teachers Pay Teachers: they pay out monthly, with payout minimums.
- Survey and microtask sites: an AI doing tasks meant for humans is dishonest and breaks their terms.
- Open-source bounties: rule 6 keeps us in this repository.
- Gumroad: it has a payout minimum (still to verify).

## Recommendation: Etsy digital sprint (E2 + E3)

- **Catalog:** 20–25 listings, split between niche printables (PDF) and editable Canva templates (delivered as a template link inside a PDF).
- **Targeting:** phrases that are both **seasonal and niche**, so people are searching now and few shops compete. Examples: "dog groomer holiday gift certificate Canva", lash tech or massage gift certificates, price signs for craft-fair vendors, holiday gift or budget trackers for specific hobbies.
- **Pricing:** worst case, Etsy keeps:
  - $0.20 renewal when an item sells
  - 6.5% transaction fee
  - 3% + $0.25 payment processing
  - 15% Offsite Ads, when a sale comes from those ads

  So net ≈ **0.755 × price − $0.45**. ~~The lowest price is $2.49~~ (superseded: the minimum is now $3.99, see the update at the top).
- **Why:** the shop's buyers are strangers already searching on Etsy. A digital download needs no fulfillment, and the work suits AI helpers plus the Canva connector. Shaky's time goes into uploading and a few checks.

### What raises confidence (medium → medium-high)
1. **Check demand first.** Only build for phrases where competitor listings show proof of sales (reviews, "in carts", Bestseller badges) and there aren't too many results. Etsy blocks our page fetches (HTTP 403), so Shaky pulls numbers from the free eRank tool.
2. **Seasonal + niche** phrases, not broad ones.
3. **Breadth:** 20–25 listings at launch, then a few more every couple of days.
4. **Listings that convert:**
   - Mockup first image with a benefit line, 5–10 images, a short Canva video.
   - The exact buyer phrase at the start of the title, all 13 tags, every attribute filled in.
5. **Refund-proofing:**
   - Templates use **only free Canva elements**, so any buyer can edit them on a free account. Pro elements would show watermarks for buyers without Pro, a common cause of refunds. Shaky's Pro is only for our production speed.
   - Each download is a PDF with the template link and a 3-step how-to.
   - Listings say "digital, no physical item" clearly, and returns are set to "not accepted".
6. **Shop trust refresh:** banner, icon, About section, policies, FAQ.
7. **Free traffic:** Etsy Offsite Ads stay on (no upfront cost; Etsy takes a fee only when a sale comes from them) and a new Pinterest business account for the shop, pinned by hand by Shaky.
8. **Adjust as we go:** Shaky screenshots Etsy Stats on days 2 and 4. We rewrite listings with no views and make more versions of the ones getting views.

"High" confidence would need paid ads or an existing base of reviews. Both are out of scope.

### Compliance checklist for every listing
- An AI-use disclosure in the description (Etsy requires it).
- No trademarks, brands, characters or celebrity names. Original layouts only, and no resold Canva templates.
- No fake reviews, and no reviews traded for discounts.
- Price ≥ $3.99 (was $2.49 before the Mexico fee correction). Free Canva elements only.

## Open question: how the team reaches the store
Agents can't log in to Etsy.
- **Default:** the team makes a ready-to-paste kit for each listing (files, title, 13 tags, description, images) in `listings/<slug>/`, and Shaky uploads it. Etsy's "copy listing" feature makes this faster.
- **Later option:** Etsy's Open API, which needs a developer app approved by Etsy. Probably too slow for this challenge.

## Sources
- [Etsy House Rules: AI disclosure](https://www.etsy.com/ca/new-guidelines)
- [Etsy payment account reserves (ChannelX)](https://channelx.world/2021/01/etsy-payment-account-reserve-introduced)
- [Etsy reserve levels (Retail Gazette)](https://www.retailgazette.co.uk/?p=141770)
- [Selling Canva templates on Etsy (FitSmallBusiness)](https://fitsmallbusiness.com/how-to-sell-canva-templates-on-etsy/)
- Fee percentages are from general knowledge and still need checking against Etsy's current fee page.
