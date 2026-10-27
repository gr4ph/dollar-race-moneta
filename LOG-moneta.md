# Team Moneta: Log

**Project:** Etsy shop printmystyledesigns.etsy.com, digital downloads (ongoing; the 7-day challenge ended 2026-10-27)
**Project start:** 2026-10-27 · **Deadline:** none
**Net earned so far:** $0.00 · **Live listings:** 0

## Brief for Shaky

_The manager rewrites this at the end of every session. Keep it short enough to read on a phone._

- **Status:**
  - New rulebook **approved and live** in `CLAUDE.md`.
  - Canva connection confirmed: the team can reach your account. The `Moneta – Etsy` folder doesn't exist yet; the builder will create it.
  - Ready to start building as soon as keywords are checked.
- **Net earned so far:** $0.00 · **Live listings:** 0
- **RFC:** none, per your accountant. So we price for Etsy withholding **20% ISR** on every sale (and 16% IVA on the rare Mexican buyer).
  - Etsy doesn't hold that 20% and release it later. It sends it to the SAT. Whether you can credit it against your own taxes, or whether it's final, is a question for your accountant. Mexican tax sites tie the "final payment" option to LISR art. 113-B.
  - Prices: **$3.99 minimum**, Canva templates $4.99–$8.99. That leaves roughly $1.13–$3.40 per sale.
- **Top keyword picks (still to be checked):** dog groomer, pet sitter and house cleaning holiday gift certificates; craft-show price list sign; bakery Christmas cookie order form.
- **Decisions I need from you:**
  1. Is your Pinterest business account free to use for this shop? (See R7.)
- **New requests:**
  - **Now:** R1 (shop snapshot) and R5 (Etsy API key, which replaces most of R6).
  - **Later:** R3 (one Etsy setting) and R7 (Pinterest).

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

**R3. Shop settings (before the first listings go live)**
1. Nothing to do for returns: Etsy doesn't allow return policies on digital items.
2. **Settings → Offsite Ads**: leave it **on**. You only pay (15%) when a sale comes from those ads, and you can opt out anytime while the shop is under $10k a year.
3. Listing currency is already USD. Nothing to do.

**R4. Canva check: DONE.** Connected and working. The builder creates the `Moneta – Etsy` folder.

**R5. Etsy API key (now, about 10 min, on a computer)**
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
2. Open **Keyword Tool**. For each ★ phrase in `research/keyword-candidates.md`, note the **searches, competition and CTR**, or screenshot them.
3. Send the numbers back.

**R7. Pinterest (after the first listings are live)**
Pinterest is a search engine for ideas, and printables and templates are a big category there. Each pin links to a listing, so it brings in buyers who aren't on Etsy.
1. Reply: is your Pinterest business account free to use for this shop, or is it tied to another brand? Don't send the password; the team never logs in.
2. If it's free: **Settings → Claimed accounts → Etsy → Claim** and log in to Etsy. Your listings then show as linked to your profile.
3. Update the profile name and bio. I'll send the text to paste.
4. For each listing, we prepare 2–3 pin images (1000×1500) plus a title, description and link. You post them by hand, a few a day. CLAUDE.md doesn't allow automated posting.

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
- **Researcher (sonnet):** drafted `research/keyword-candidates.md` (50 phrases, top 15 ★) and `research/verification-notes.md`. Etsy blocks us, so demand signals are thin; every competition rating is a guess until checked through the API or eRank.
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
