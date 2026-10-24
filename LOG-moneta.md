# Team Moneta: Log

**Start date:** 2026-10-24
**Deadline:** 2026-10-31 _(Shaky will reset this once everything is ready)_
**Earned so far:** $0.00

## Brief for Shaky

_The manager rewrites this at the end of every session. Keep it short enough to read on a phone._

- **Status:** Brainstorm paused (Session 1). Nothing built yet. Leading plan is an **Etsy digital sprint**: 20–25 niche printables and editable Canva templates in your existing shop. Full analysis is in `IDEAS-moneta.md`.
- **Earned so far:** $0.00
- **Agreed so far:**
  - Trading and betting are rejected (rule 4, and no customer). Etsy print on demand is replaced by digital downloads in the same shop.
  - A sale counts once it's in the Etsy balance, and $1 means net after fees. So the **lowest price is $2.49**.
  - Digital only, not customizable, few refunds. No paid ads, and no personal network.
  - You pay Etsy listing fees; the team budget stays $0.
  - Canva templates use free elements only, so buyers don't need Pro. Your Canva Premium is for our production speed.
- **Decisions I need from you (when we resume):**
  1. Final go on the Etsy digital sprint.
  2. How the team reaches the store. My default: we make ready-to-paste listing kits and you upload them.
- **New requests:** see Requests for Shaky. None are needed until we resume.

## Team

_Proposed lineup. Not created yet; it gets set up in `.claude/agents/` when the brainstorm resumes._

| Role | Model | Job |
|---|---|---|
| Manager (me) | strongest model | Plans, decides, talks to Shaky, final review |
| Researcher | sonnet | Validates keywords and demand, checks platform facts |
| Builder | sonnet | Makes the printable PDFs and Canva templates, mockups, video |
| Marketer | haiku | Writes listing titles, the 13 tags and descriptions from the playbook template |
| Reviewer | haiku | Read-only check against the rules and Etsy policy before anything goes to Shaky or goes public |

## Payments received

_Shaky adds each confirmed payment here._

| Date | Amount | From / via | Confirmed by Shaky |
|------|--------|------------|--------------------|

## Requests for Shaky

_Open requests go here as numbered steps. Shaky marks each one DONE when finished._

**R1. Etsy shop details (needed when we resume)**
1. Open the Etsy app → **Shop Manager**.
2. Reply with: your shop link, the shop currency, and whether vacation mode is off.
3. Tell me how you'd like the team to work with the store. Default: we put a ready-to-paste kit per listing in the repo and you upload it.

**R2. eRank keyword check (after we send the keyword list)**
1. Go to **erank.com** → **Sign up free** → connect your Etsy shop.
2. Open **Keyword Tool**.
3. For each phrase in `research/keyword-candidates.md` (coming next session), type it in and screenshot the result, or copy three numbers: **searches, competition, CTR**.
4. Paste the numbers into the chat or send the screenshots.

**R3. Canva check**
1. Confirm that the Canva account connected to this Claude workspace is the one with Premium.

**R4. Etsy settings (before the first listings go live)**
1. Shop Manager → **Settings → Policies**: set returns to "not accepted" for digital items.
2. Shop Manager → **Marketing → Offsite Ads**: leave it **on**. It costs nothing unless a sale comes from it.
3. Later: create a free **Pinterest business account** for the shop. I'll send the exact steps when the listings are ready.

## Earlier sessions

_Summary of sessions older than the last 3, a few sentences total. The manager rolls old entries in here._

## Session log

### Session 1 — 2026-10-24
Goal: Set dates, review ideas, and agree on a direction. Shaky paused the session partway through the brainstorm.
Team activity:
- Manager worked solo. No helpers were spawned, to save usage while the direction was still open.
- Reviewed Shaky's 3 ideas and proposed 8 of my own (A, B, C, E1–E5).
- Checked facts by web search on Etsy reserves, Etsy's AI-disclosure rule and Canva template licensing.
- Found that Etsy blocks direct page fetches (HTTP 403), so demand research needs data from Shaky (eRank).

Decisions:
- **Rejected trading and betting:** no customer, needs capital, and rule 4 bans them.
- **Replaced Etsy print on demand with Etsy digital downloads (E2 + E3):** digital needs no fulfillment, the shop's buyers are strangers already searching, and the work suits AI plus Canva.
- **Lowest price $2.49:** in the worst case, net ≈ 0.755 × price − $0.45, and $1 must be net.
- **Free Canva elements only:** keeps buyers from needing Pro, which avoids refunds.
- **No paid ads, no personal network:** Shaky's call.
- **Agent Team Starter Kit (A) parked as a backup.**

Next steps:
1. Resume the brainstorm with Shaky and get the final go and the store link (R1).
2. Create `.claude/agents/` (the 4 helpers above) and `PLAYBOOK-moneta.md`.
3. Researcher drafts `research/keyword-candidates.md` (40–50 phrases that are both seasonal and niche) and `research/platform-facts.md` (check Etsy fees against Etsy's current fee page).
4. Shaky runs the eRank check (R2). Then we pick the top 20–25 phrases and start building listing kits.

Earned so far: $0
