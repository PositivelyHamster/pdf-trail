# BRIEF.md — how to write a PDFTrail blog post

Read FACTS.md first. Everything you state about the product comes from there.
Then read the calendar row you were given: slug, title, primary keyword, pillar, campaign token.

## Voice and language

- First person, written by Arkya Ghosh. Plain English, ASD-STE100 style: sentences of 20 words or fewer, active voice, one meaning per word. No sentence over 35 words (the validator fails it).
- Problem first. The first paragraph (the standfirst) describes the reader's problem in concrete terms. PDFTrail is not named until the reader knows why the obvious routes fail.
- Honest. Every alternative gets a fair sentence about when it is fine. The disclosure "PDFTrail is my app" appears once, near the first product mention.
- No hype words: "revolutionary", "seamless", "powerful", "cutting-edge", "game-changer". No exclamation marks.
- Numbers only when they come from FACTS.md.

## Structure (in this order)

1. Standfirst paragraph: the problem, 40-80 words.
2. One or two paragraphs on why the obvious routes fail (retyping, copy-paste, upload sites, whichever apply). End with "The short answer:" in bold and one sentence.
3. `## ` section: the real options, honestly compared (2-4 options, one bold lead-in each).
4. `## ` section: the PDFTrail walkthrough as a numbered list. Always include the review step before export.
5. `{{figure}}` placed after the walkthrough (or leave it out; the generator places it after the first section).
6. `## ` section: why it works, one paragraph of mechanism from FACTS.md (positioned text, no OCR guessing for born-digital; OCR plus Table Review for scans).
7. Optional `## ` section specific to this document type: what to check after export, common gotchas, what to do with the spreadsheet next.
8. FAQ: 3-6 questions in the front matter. Real questions a searcher asks. Answers 1-3 sentences, complete on their own (they are shown to search engines as FAQ rich results). At least one answer says "on your Mac" or "on-device".
9. Do NOT write a closing CTA or "Get PDFTrail" section. The template adds it.

## SEO rules (the validator enforces the mechanical ones)

- `title`: 60 characters or fewer, contains the primary keyword.
- `description`: 70-155 characters, contains the primary keyword, no exclamation mark.
- Primary keyword appears in: the title, the description, the first 100 words, at least one H2, and `figure_alt`. Use it naturally, at most 6-8 times in the whole post.
- Body length: 900-1500 words, FAQ excluded.
- 3-7 H2 sections. H3 only inside a long H2.
- Exactly one figure, chosen from `assets/screenshots/web/`: 01_table_review.jpg (the review screen), 02_conversion_graph.jpg (conversion progress), 03_exports_ready.jpg (exported files), 04_batch_convert.jpg (batch folder), 05_empty_canvas.jpg (empty app window), 06_pricing.jpg (unlock screen), 07_no_signup_collage_web.jpg (no-signup collage). `figure_alt` describes what is on screen, 40+ characters, includes the keyword naturally.
- 2-3 internal links, written as `[text](/blog/<slug>/)`, to posts that are live or scheduled before this one. Always link your pillar's hub page and one sibling. The generator adds a "Related guides" list, so do not write one.
- Exactly one external citation from the allow-list in `config.json` (Microsoft, Apple, Tabula, camelot, pdfplumber, Adobe, Google support, Indian government portals, SEC). Link the page you actually mean.
- Never write an App Store link in the body.

## Markdown subset

Supported: `## H2`, `### H3`, paragraphs, `- ` bullet lists, `1. ` numbered lists, `**bold**`, `*italic*`, `` `code` ``, `[text](url)`, one `{{figure}}` line on its own.
Not supported (the validator rejects them): tables, blockquotes, raw HTML, `![images]()`, code fences, H1, H4.

## Front matter (copy this skeleton)

```
---
title: SBI Bank Statement PDF to Excel on Mac
description: Convert an SBI bank statement PDF to Excel on your Mac without uploading it. Why copy-paste fails, and the on-device route step by step.
date: 2026-09-24
time: 18:00
kicker: Field guide
pillar: P1
primary_keyword: sbi bank statement pdf to excel
figure: 01_table_review.jpg
figure_alt: Reviewing the detected SBI bank statement transaction table in PDFTrail on macOS before exporting to Excel
figure_caption: The review step, where you check the table before anything is exported.
campaign: bl-sbi
status: draft
faq:
  - q: Does this work with a scanned SBI statement?
    a: Yes. Scanned pages have no text layer, so PDFTrail runs OCR on your Mac and shows the table for review before export.
  - q: Do I need an internet connection?
    a: No. Everything runs on your Mac. Nothing leaves the device.
  - q: How much does it cost?
    a: It is free to try, with 10 free Excel exports. The full version is a $24 one-time unlock, no subscription.
---
```

Optional keys: `seo_title` (if the `<title>` should differ from the H1), `summary` (blog index card text, defaults to description), `updated` (YYYY-MM-DD), `og_image` (file in assets/screenshots/full/), `cta_label`, `read_time`, `keywords` (comma list of secondary terms; not emitted, for the reviewer).

Kickers: `Field guide` (how-to), `Comparison` (tool vs tool), `Engine notes` (how the engine works), `Release notes`.

## Delivery

Save the file as `_blog/drafts/<slug>.md` with `status: draft`. Run `python3 _blog/build.py validate _blog/drafts/<slug>.md` and fix every FAIL. Report the WARN lines you left in place and why.
