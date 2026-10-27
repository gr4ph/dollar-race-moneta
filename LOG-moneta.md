# Team Moneta: Log

**Project:** Etsy shop printmystyledesigns.etsy.com, digital downloads (ongoing; the 7-day challenge ended 2026-10-27)
**Project start:** 2026-10-27 · **Deadline:** none
**Net earned so far:** $0.00 · **Live listings:** 0

## Brief for Shaky

_The manager rewrites this at the end of every session. Keep it short enough to read on a phone._

- **Status:** The team is set up for the Etsy business: 4 helpers, a playbook, a fact file and a listing template. A new rulebook is waiting for your review: `drafts/CLAUDE-proposed.md`. The keyword list is in `research/keyword-candidates.md`.
- **Net earned so far:** $0.00
- **Pricing corrected:**
  - With a Mexican bank, no RFC on file and USD listings, the worst case keeps only about 47% of the price minus about $0.75.
  - The new minimum price is **$3.99**. Printables sell for $3.99–$5.99, Canva templates for $4.99–$8.99.
- **RFC and RESICO (facts only; your accountant decides):**
  - Without an RFC, Etsy withholds **20% ISR** on every sale. With one, it withholds 2.5%, plus 8% IVA only on Mexican buyers.
  - **Paying with PayPal on Etsy doesn't avoid this.** It's only a way for buyers to pay. Etsy pays you out to your bank, and the withholding applies either way.
  - With an RFC on file, Etsy sends you a CFDI for the taxes it withheld. That's a record of withholding, not an invoice to your customers, so it shouldn't clash with the invoices your accountant issues.
  - The open question for your accountant is in R2.
- **Decisions I need from you:**
  1. Approve or change `drafts/CLAUDE-proposed.md`. It replaces CLAUDE.md once you say yes.
  2. The R2 accountant answer about the RFC.
- **New requests:** R1–R7 below. R1, R2 and R4 are needed now.

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

**R2. RFC question for your accountant (now, high priority)**
Without an RFC, Etsy withholds 20% of every sale. Send them this:
```
I sell digital downloads on Etsy (mostly to US buyers). Etsy withholds 20% ISR
when no RFC is on file, or 2.5% ISR (plus 8% IVA on Mexican buyers only) when
an RFC is on file, and then issues a CFDI for what it withholds. I'm in RESICO.
1) Should I add my RFC in Etsy? 2) Can this income stay under RESICO, or does
it need the "Plataformas Tecnológicas" regime? 3) How do Etsy's withholding
CFDIs fit with the invoices you issue?
```
Then, if the answer is yes: open the same RFC screen you screenshotted, tap **Edit**, and enter it. Don't send the RFC to the team.

**R3. Shop settings (before the first listings go live)**
1. **Settings → Policies**: for digital items, set returns and exchanges to **not accepted**.
2. **Marketing → Offsite Ads**: leave it **on**. You only pay when a sale comes from those ads.
3. Listing currency is already USD. Nothing to do.

**R4. Canva check (now)**
1. Confirm the Canva account connected to Claude is your Premium account.
2. In Canva, create a folder named `Moneta – Etsy`, or let the builder create it.

**R5. Etsy API key (after the first listings are live)**
The key lets the team pull keyword and competitor data and later create draft listings for you to approve.
1. On a computer, go to **etsy.com/developers** → **Create a new app**.
2. App name: `Moneta Shop Tools`. Describe it as a personal tool for managing your own shop. Pick "personal use".
3. Wait for Etsy's approval email.
4. In Claude: open this session's **environment menu** (title bar) → **Edit** → **Network secrets** (or environment variables) → add `ETSY_API_KEY` = `keystring:shared_secret` from the Etsy app page.
5. Never paste the key in chat or the repo.

**R6. eRank (only if the API isn't ready yet)**
1. Go to **erank.com** → sign up free → connect your Etsy shop.
2. Open **Keyword Tool**. For each ★ phrase in `research/keyword-candidates.md`, note the **searches, competition and CTR**, or screenshot them.
3. Send the numbers back.

**R7. Pinterest (later)**
When listings are live, I'll send steps for a free Pinterest business account for the shop. Nothing to do yet.

## Earlier sessions

- **Session 1 (2026-10-24), challenge era:**
  - Reviewed your 3 ideas: Etsy print on demand replaced by digital downloads; trading and betting rejected (rule 4, no customer).
  - Proposed 8 more and picked an Etsy digital sprint (niche printables plus Canva templates). The details are in `IDEAS-moneta.md`.

## Session log

### Session 2 — 2026-10-27
Goal: Switch from the challenge to the ongoing Etsy business, and set up everything the team needs to run it.

Team activity:
- **Manager:**
  - Checked Etsy's Mexico fees and withholding on help.etsy.com and recalculated pricing.
  - Wrote the 4 agent definitions, `PLAYBOOK-moneta.md`, `research/platform-facts.md`, the listing template and the rulebook draft.
  - Confirmed the Etsy API host is reachable from the cloud environment (it needs a key). Etsy's web pages still block us.
- **Researcher (sonnet):** drafted `research/keyword-candidates.md` and `research/verification-notes.md`.
- **Reviewer (haiku):** checked the requests and the rulebook draft.

Decisions:
- **Price floor $3.99**, because Mexico processing fees, the 2.5% conversion fee and the 20% ISR without an RFC cut the net sharply.
- **Listings via kits now, Etsy API later:** kits work today. The API saves your time later, but needs Etsy's approval.
- **Draft-only through the API:** you stay in control of what gets published.
- **Rulebook rewrite kept as a draft:** CLAUDE.md is yours to approve.

Next steps:
1. Get R1, R2 and R4 back from you.
2. Validate the ★ keyword phrases (API or eRank), then pick the first 10 products.
3. Builder and marketer make the first 5 listing kits, with a reviewer pass. Write the shop refresh copy (About, announcement, FAQ, banner).
4. Once you approve it, replace CLAUDE.md with the draft.

Net earned so far: $0
