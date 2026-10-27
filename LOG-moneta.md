# Team Moneta: Log

**Project:** Etsy shop printmystyledesigns.etsy.com, digital downloads (ongoing; the 7-day challenge ended 2026-10-27)
**Project start:** 2026-10-27 · **Deadline:** none
**Net earned so far:** $0.00 · **Live listings:** 0

## Brief for Shaky

_The manager rewrites this at the end of every session. Keep it short enough to read on a phone._

- **Status:** The rebrand and catalog plans are ready for your decision: `BRAND-moneta.md` and `CATALOG-moneta.md`. Building starts as soon as you pick a name.
- **Net earned so far:** $0.00 · **Live listings:** 0
- **Positioning (my recommendation):** templates and printables for **small businesses, makers and service pros**.
  - Main line: editable Canva templates, each made for a specific trade (gift certificates, price lists, signs, order and intake forms).
  - Second line: business printables (vendor kits, logs, a 2027 content calendar).
  - Every seasonal item gets an evergreen twin. Home printables are parked because most sell for $1–$3, below our $3.99 minimum.
- **Name shortlist:** ★ **TillAndTag**, OpenSignStudio, LedgerAndLinen. All 24 ideas are in `research/name-ideas.md`.
- **Holiday timing:**
  - Thanksgiving is nearly too late; only a closure-notice set can make it, if it's live by Nov 3.
  - Christmas wave 1 (13 listings) must be live by **Nov 10**.
  - New Year wave 2 (7 listings) by **Nov 25**.
- **Keywords:** split into `research/keywords-seasonal.md` and `research/keywords-evergreen.md`, as you asked.
- **Decisions I need from you:**
  1. Approve the positioning, or tell me what to change.
  2. Pick a name (R8).
- **New requests:**
  - **Now:** R8 (name + trademark check + rename) and R5 (check for an existing Etsy app).
  - **Still open:** R1 (shop snapshot).

## Team

| Role | Model | Job | Defined in |
|---|---|---|---|
| Manager (me) | strongest model | Plans, decides, talks to Shaky, final review, commits | `CLAUDE.md` |
| Researcher | sonnet | Keyword and demand validation, competitor scans, fact checks | `.claude/agents/researcher.md` |
| Builder | sonnet | Printable PDFs and Canva templates (via the Canva connector), mockups, delivery PDFs, API scripts | `.claude/agents/builder.md` |
| Marketer | haiku | Listing titles, 13 tags, descriptions, shop copy, Pinterest text, customer reply drafts | `.claude/agents/marketer.md` |
| Reviewer | haiku | Read-only checklist pass on anything going to Shaky or going public | `.claude/agents/reviewer.md` |

## Payments received

_Shaky adds each confirmed sale here._

| Date | Listing | Price (USD) | Net received | Confirmed by Shaky |
|------|---------|-------------|--------------|--------------------|

## Requests for Shaky

_Open requests as numbered steps. Shaky marks each one DONE when finished._

**R1. Shop snapshot (now)**
This tells me what's left from the old shop: reviews, sales, branding.
1. Etsy → **Shop Manager → Dashboard**: screenshot.
2. **Shop Manager → Stats** → set the date range to "All time": screenshot.
3. **Shop Manager → Settings → Info & Appearance**: screenshot the top (shop name, title, icon, banner).
4. Tell me whether vacation mode is on.
5. Tell me roughly how many minutes a week you can spend uploading listings.

**R2. RFC question: DONE.** Answer: no RFC for now, so Etsy withholds 20% ISR. Pricing is set for that.

**R3. Shop settings: DONE.** Offsite Ads are on, listing currency is USD, and digital items can't have return policies anyway.

**R4. Canva check: DONE.** Connected and working. The builder creates the `Moneta – Etsy` folder.

**R5. Etsy API key (now, about 10 min, on a computer)**
**First, check whether you already have an app:** open **etsy.com/developers/your-apps**, signed in to the shop's Etsy account.
- **If an app is listed** and its status is approved, reuse it: skip to step 4 and use its keystring and shared secret. You can't create a second seller app while one exists.
- **If it says pending or rejected,** tell me what it says.
- **If nothing is listed,** do steps 1–5.

Also, Shop Manager → Apps → Connected apps may still show the old Printify connection. You can disconnect it there; that page is separate from developer apps.

The key lets the team check keywords and competitors on Etsy itself, which we can't do today, so it replaces most of the eRank work. Later, after a one-time authorization, it lets us create draft listings for you to approve. It can't publish or spend anything.
1. On a computer, go to **etsy.com/developers** → **Create a seller app** (for your own shop only; it's usually approved within minutes. Don't pick "personal app", which takes much longer).
2. Read the API terms at etsy.com/legal/api before accepting. We couldn't open them from here.
3. App name: `Moneta Shop Tools`. Description to paste:
```
Private tool to create draft listings and read stats for my own shop. I review and publish every listing myself.
```
4. In Claude: open this session's **environment menu** (title bar) → **Edit** → **Network secrets** (or environment variables) → add a variable named `ETSY_API_KEY` whose value is your keystring and shared secret joined by a colon:
```
<keystring>:<shared_secret>
```
5. Never paste the key in chat or the repo.

**R6. eRank (only if Etsy rejects the API app or it doesn't work)**
1. Go to **erank.com** → sign up free → connect your Etsy shop.
2. Open **Keyword Tool**. For each ★ phrase in `research/keywords-seasonal.md`, note the **searches, competition and CTR**, or screenshot them.
3. Send the numbers back.

**R7. Pinterest (after the first listings are live)**
Pinterest is a search engine for ideas, and printables and templates are a big category there. Each pin links to a listing, so it brings in buyers who aren't on Etsy.
1. Reply: is your Pinterest business account free to use for this shop, or is it tied to another brand? Don't send the password; the team never logs in.
2. If it's free: **Settings → Claimed accounts → Etsy → Claim** and log in to Etsy. Your listings then show as linked to your profile.
3. Update the profile name and bio. I'll send the text to paste.
4. For each listing, we prepare 2–3 pin images (1000×1500) plus a title, description and link. You post them by hand, a few a day. CLAUDE.md doesn't allow automated posting.

**R8. Pick the shop name and rename (now)**
1. Read `BRAND-moneta.md` and reply with the name you want: TillAndTag, OpenSignStudio, LedgerAndLinen, or your own idea.
2. Trademark check (2 min): go to **tmsearch.uspto.gov**, type the name, and check that nothing live in a similar field (paper goods, templates, software) comes up.
3. Rename: **Shop Manager → Settings → Your shop → Shop name → Edit**. Type the name; Etsy tells you if it's free. Save.
4. Tell me it's done. The team then builds the logo, banner and shop text to match.
   (Etsy allows 5 renames on your own, and old links redirect automatically.)

## Earlier sessions

- **Session 1 (2026-10-24), challenge era:**
  - Reviewed your 3 ideas: Etsy print on demand replaced by digital downloads; trading and betting rejected (rule 4, no customer).
  - Proposed 8 more and picked an Etsy digital sprint (niche printables plus Canva templates). The details are in `IDEAS-moneta.md`.

## Session log

### Session 3 — 2026-10-27
Goal: Rebrand proposal (name + identity) and a catalog plan mixing seasonal and evergreen products.

Team activity:
- **Researcher (sonnet):** wrote `research/catalog-research.md`, covering Etsy rename rules, how to check for an existing developer app, the seasonal calendar for Nov 2026 to Dec 2027 with lead times, evergreen demand signals, and the evidence on positioning.
- **Marketer (haiku):** wrote 24 shop names, each with one web search for conflicts, in `research/name-ideas.md`.
- **Manager:**
  - Picked the positioning.
  - Added and checked 4 names of my own: TillAndTag is clear; ShopkeepStudio is ruled out (ShopKeep is a point-of-sale brand).
  - Wrote `BRAND-moneta.md` and `CATALOG-moneta.md`.
  - Split the keywords into seasonal and evergreen lists, as Shaky asked.
- **Reviewer (haiku):** checked the brand, catalog and keyword files. It failed them on 4 blocking points, all claims stated more strongly than the research supports. All 4 are fixed, along with the non-blocking notes (pricing bands, no-advice notes on forms, an event name swapped for a generic phrase).

Decisions:
- **Small-business focus, two formats** (Canva templates first, business printables second). It fits the $3.99 minimum, narrow niches suit a new shop, and the buyer stays the same across products. Consumer home printables are parked because of low prices and entrenched competitors.
- **Product families with evergreen twins:** one design gives many listings, and each holiday item keeps selling after the holiday.
- **Thanksgiving mostly skipped; Christmas wave by Nov 10:** business buyers buy 2–4 weeks before consumers, and new listings need time to show up in Etsy search.

Next steps:
1. Shaky picks the name and renames the shop (R8), and checks for an existing Etsy app (R5).
2. Builder creates the brand kit (logo, banner) and the first base design: a holiday gift certificate with 7 trade versions.
3. Marketer writes the kits for wave 1. Reviewer checks them, then they go to Shaky.

Net earned so far: $0

### Session 2 — 2026-10-27
Goal: Switch from the challenge to the ongoing Etsy business, and set up everything the team needs to run it.

Team activity:
- **Manager:**
  - Checked Etsy's Mexico fees and withholding on help.etsy.com and recalculated pricing.
  - Wrote the 4 agent definitions, `PLAYBOOK-moneta.md`, `research/platform-facts.md`, the listing template and the rulebook draft.
  - Confirmed the Etsy API host is reachable from the cloud environment (it needs a key). Etsy's web pages still block us.
- **Researcher (sonnet):** drafted `research/keywords-seasonal.md` (50 phrases, top 15 ★) and `research/verification-notes.md`. Etsy blocks us, so demand signals are thin; every competition rating is a guess until checked through the API or eRank.
- **Reviewer (haiku):** checked the brief, the requests, the rulebook draft and the pricing table. It failed them on 3 blocking points: unsourced tax claims, a table rounding mismatch, and weakened "run by AI" wording. All 3 are fixed, along with most non-blocking notes.

Decisions:
- **Price floor $3.99**, because Mexico processing fees, the 2.5% conversion fee and the 20% ISR without an RFC cut the net sharply.
- **Listings via kits now, Etsy API later:** kits work today. The API saves your time later, but needs Etsy's approval.
- **Draft-only through the API:** you stay in control of what gets published.
- **Follow-up, same day:**
  - You approved the rulebook, so it's now `CLAUDE.md`.
  - No RFC, per your accountant, so pricing keeps the 20% withholding.
  - Canva connection confirmed.
  - API key moved to "now", because it replaces eRank for keyword checks.
- **Rulebook rewrite kept as a draft:** CLAUDE.md is yours to approve.

Next steps:
1. Get R1 and R5 back from you.
2. Validate the ★ keyword phrases (API or eRank), then pick the first 10 products.
3. Builder and marketer make the first 5 listing kits, with a reviewer pass. Write the shop refresh copy (About, announcement, FAQ, banner).

Net earned so far: $0
