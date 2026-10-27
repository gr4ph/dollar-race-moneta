# Team Moneta: Playbook

How the team does its recurring jobs. Helpers read this instead of working things out from scratch. The manager updates it when we learn something.

## 0. Basics

- **What we sell:** digital downloads on Etsy (printmystyledesigns.etsy.com). There are two kinds: niche **printables** (PDF) and editable **Canva templates** (the buyer gets a PDF containing the template link).
- **Who buys:** mostly US buyers, prices in USD. Not customizable: we do no work per order.
- **Rules:** `CLAUDE.md` always wins. When in doubt, the manager writes it as a question for Shaky.
- **File layout:**
  - `research/`: keyword lists, platform facts, competitor notes
  - `listings/<slug>/`: one folder per product
    - `listing.md`: the copy and settings Shaky pastes, from `listings/_TEMPLATE/listing.md`
    - `files/`: what the buyer downloads
    - `images/`: mockups, 2000×2000 px or larger, JPG/PNG
  - `drafts/`: anything waiting for Shaky's approval
- **Commits:** the manager commits after each finished unit of work. Message style: `Listings: add 3 groomer gift certificate kits`.

## 1. Briefing a helper (manager)

Every brief contains:
1. **Role + one-line goal**, e.g. "Researcher: validate 10 phrases for Canva gift certificates."
2. **Inputs:** the exact files to read.
3. **Output:** the exact file path(s) and format.
4. **Done means:** copied from the matching section below.
5. **Report:** the word limit and what to include.

Use smaller models for routine work: researcher and builder on sonnet, marketer and reviewer on haiku. Only delegate work that is big enough or can run in parallel.

## 2. Keyword validation (researcher)

1. Start from a theme: a trade, hobby or audience × a season or use.
2. Write 5–10 phrases the way a buyer types them, for example "lash tech gift certificate template canva".
3. For each phrase, collect demand and competition signals:
   - **Best:** the Etsy API (`findAllListingsActive` with `keywords`): total result count, plus favorites and reviews on the top listings.
   - **Next best:** eRank numbers that Shaky sends (searches, competition, CTR).
   - **Fallback:** web search (Etsy listings in Google with review counts, Pinterest saves, lists of best-selling printables).
4. **Keep a phrase** when it shows proof of demand (top listings have reviews, are in carts or carry a Bestseller badge) and the result count is manageable. As a rule of thumb, fewer than about 5,000 Etsy results is good, under about 20,000 is fine for a strong niche, and anything above is too broad.
5. **Reject a phrase** if it contains any trademark, brand, character, celebrity or sports team.

**Done:** a table of phrase | type | signals (with numbers) | keep/reject | reason. Anything unverified is marked UNVERIFIED.

## 3. Fact check (researcher)

- Official sources first: help.etsy.com, etsy.com/legal, etsy.com/developers, canva.com/policies.
- Every fact gets a source link and the date it was checked. Facts go in `research/platform-facts.md`.

## 4. Build a printable (builder)

- Letter size (8.5×11 in) **and** A4 versions, as a vector PDF made in Canva and exported as "PDF Print".
- Clean, readable, ink-friendly: no full-page dark backgrounds unless that's the selling point.
- Include a small footer with the shop name. No personal data.
- **Done:** PDFs in `files/`; they open correctly and every page is checked; under 20 MB each.

## 5. Build a Canva template (builder)

- Original layout built from scratch in Canva, inside the "Moneta – Etsy" folder.
- **Free elements only** inside the sold template: free fonts, free graphics, free photos. Pro tools are fine for production.
- Placeholder text explains what to replace, e.g. "YOUR BUSINESS NAME".
- Share it as a **template link** (Share → Template link).
- The delivery PDF (`files/<slug>-access.pdf`) holds:
  1. The template link as a big button.
  2. 3 steps: click the link → log in to a free Canva account → "Use template" and edit.
  3. Licence: personal and small-business use; the buyer may not resell the template.
- **Done:** the link opens as a copy in a free account with no Pro watermark, and the PDF link works.

## 6. Listing kit (marketer + builder)

Fill in `listings/_TEMPLATE/listing.md`:
- **Title formula** (up to 140 characters, the most important words first): `<exact buyer phrase> | <second phrase> | <format: Editable Canva Template / Printable PDF> | <use or occasion>`.
- **Tags:** exactly 13, each 20 characters or fewer, all different, long-tail. No trademarks. Naming the format descriptively ("canva template", "editable pdf") is fine; never use it as our branding.
- **Description:**
  1. A one-line hook saying what it is and who it's for.
  2. What you get: files, sizes, number of pages.
  3. How it works, with the 3 steps.
  4. Requirements: a free Canva account, or a PDF reader and printer.
  5. "Digital download, no physical item will be shipped."
  6. Licence line.
  7. **AI disclosure:** "Designed by our team with the help of AI tools."
  8. A short FAQ.
- **Images:** at least 5:
  1. A hero mockup with a 3–5 word benefit line.
  2. What's included.
  3. Close-up detail.
  4. An "edit in Canva" or "print at home" explainer.
  5. Sizes and format.

  Optional: a 5–15 s Canva video.
- **Price:** follow the pricing table below.
- **Done:** every field filled in, the reviewer passes it, and Shaky can paste it without editing.

## 7. Pricing (manager decides)

Facts:
- Shop listing currency is **USD** and the bank is in **Mexico**.
- Etsy converts to MXN with a **2.5% fee**.
- Processing is **4.5% + MXN 8** per order.
- Transaction fee is **6.5%**.
- Offsite Ads take **15%**, only when a sale comes from those ads (Etsy help 360000338367).
- Listing renewal is **$0.20** when an item sells.
- ISR withholding is **20% while no RFC is on file**, 2.5% with one.
- IVA is 0% on non-Mexican buyers.
- Still unconfirmed: whether Etsy adds IVA on top of its fees. We assume it does.

Rough net per sale (conservative: MXN 8 ≈ $0.45, today ≈ $0.43; IVA on Etsy's fees assumed 16%, rate unconfirmed; the $0.20 renewal is still to be rechecked):

| Price | No RFC, Offsite Ads sale (worst case) | RFC on file, normal Etsy sale |
|---|---|---|
| $3.99 | ≈ $1.13 | ≈ $2.52 |
| $4.99 | ≈ $1.60 | ≈ $3.34 |
| $6.99 | ≈ $2.54 | ≈ $4.98 |

Formulas: no RFC worst case ≈ 0.47 × price − $0.75; with RFC, normal sale ≈ 0.82 × price − $0.75.

**Rules:**
- Minimum price **$3.99**.
- Printables $3.99–$5.99. Canva templates $4.99–$8.99. Bundles $8.99–$14.99.
- Recalculate when the RFC or fee facts change.

## 8. Review checklist (reviewer)

Blocking if any of these fail:
- [ ] No trademark, brand, character, celebrity or sports-team name anywhere: title, tags, description or images.
- [ ] No recipe, craft pattern or how-to guide product (Etsy bans AI-generated functional instructions).
- [ ] The images show a real preview of what the buyer receives.
- [ ] Every claim is true. No made-up reviews, sales, "bestseller" claims, fake discounts or features we don't have.
- [ ] The AI disclosure line is in the description.
- [ ] "Digital download, no physical item" is stated.
- [ ] Canva template: free elements only, and the delivery PDF has a working template link plus the 3 steps.
- [ ] Price is at least the floor in §7.
- [ ] No secrets, API keys or personal data (names, addresses, birth dates, tax IDs) in any file.
- [ ] Requests for Shaky are numbered steps that work on a phone, with copy-paste text ready.

## 9. Requests for Shaky (manager)

- Batch them. Add them to "Requests for Shaky" in the log as **R<n>** with a one-line purpose.
- Number the steps. Name the exact menu path, e.g. "Shop Manager → Settings → …". Put text to paste in a code block.
- Say whether it's needed now or later.
- Never ask for passwords, private keys or seed phrases. API keys go into the cloud environment settings, never into chat or the repo.

## 10. Weekly loop (once listings are live)

1. Shaky sends Etsy Stats screenshots (or we read them through the API): views, visits, favorites, orders per listing.
2. Listings with 0 views after 7 days get a new title and tags and a check of the first image.
3. Listings with views but no sales get a better hero image, a price check and an FAQ.
4. Listings with sales get 2–3 variants: another trade, season or colourway.
5. Log the results in `LOG-moneta.md` and update this playbook.

## 11. Customer messages

Shaky forwards each message. The marketer drafts a reply within the rules: polite, short and truthful. If asked, we say the shop is run by an AI team, with Shaky as its human operator. Shaky sends it. We never move a sale off Etsy.
