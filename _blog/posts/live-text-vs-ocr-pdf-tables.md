---
title: Preview Live Text vs OCR for PDF Tables on Mac
description: Live text pdf table on a Mac: what Preview's text tools do on a scanned PDF, what they leave undone, and how OCR with table rebuild differs.
date: 2026-10-19
time: 18:00
kicker: Comparison
pillar: P2
primary_keyword: live text pdf table
figure: 11_scans_clean_text_130.jpg
figure_alt: Table Review in PDFTrail with a scanned sales table on the left and the rebuilt four-column table on the right, a live text pdf table turned into rows
figure_caption: A scanned sales table next to the engine's output in Table Review. The rows and columns are rebuilt from the recognized text.
campaign: bl-livetext
status: approved
faq:
  - q: What is Live Text in Preview?
    a: Apple describes Live Text as a way to copy and use the text that appears in a photo. You select the text in Preview, Control-click, and choose Copy Text. Apple's page does not mention tables.
  - q: Can I copy a table from a scanned PDF into Excel with Live Text?
    a: You can copy the text if Preview lets you select it. A table is more than text, because the rows and columns also matter. Paste it into Excel and compare the result with the page.
  - q: How is PDFTrail different from Preview for scanned tables?
    a: PDFTrail runs OCR on your Mac, rebuilds the table from the position of the text, and shows it next to the page in Table Review. Then it writes Excel, Word, Markdown, JSON or text files.
  - q: Is OCR always right?
    a: No. OCR is good but not infallible, which is why Table Review exists. Check the digits against the page after conversion.
  - q: Do I need an internet connection?
    a: No. PDFTrail runs on your Mac. Nothing is uploaded, and there is no account.
---
Apple's help page for Preview has a tip I like. Hold Option as you select text, and you can copy one column of a table. It works on a PDF that already holds text. A scan holds pixels, which brings up the live text pdf table question: what do Preview's text tools give you on a scanned page, and what is left for you to do?

A scan stores a picture of a page. Nothing in it says "seven" or "Tents". So something has to look at the pixels and decide where the letters are. For a photo or image in Preview, that something is Live Text. Apple's [help page](https://support.apple.com/guide/preview/prvw625a5b2c/mac) describes it as a way to copy and use the text that appears in a photo: you select the text, Control-click, and choose Copy Text. The same page lists Look Up and Translate, and it says Live Text isn't available in all regions or languages. It does not mention tables.

For a scanned PDF, Apple documents a second step. File > Export > Embed Text has Preview recognize the text in an image-based PDF and embed it, so any viewer can select it. The option appears only if Preview found no text in the file. That page does not mention tables either.

Both tools do the first of two jobs. They find the text. Neither page describes the second job, which is turning that text into rows and columns. A table is not only text. It is text plus the alignment between lines, and a PDF stores positioned fragments, not a grid. Copy and paste from Preview loses that structure, and Option-select works around it one column at a time. A page with eight columns takes eight passes, and you line them up yourself.

Live Text does a good deal that Apple's page lists. You can look a word up, translate a line, call a phone number or open a website straight from a photo. None of that needs a table. If your scanned page is a letter or a receipt, Live Text may be the whole answer.

My view is simple. For one number, one line or one address, use Live Text. It is built in and it costs nothing. For a table that has to open in Excel, I want the rows rebuilt, and I want to see them next to the page.

Test it on your own page. Open the scanned PDF in Preview and choose Tools > Text Selection. If Preview lets you select the table's text, copy it and paste it into Excel or Numbers. Then look at what arrived, and compare it with the page. If nothing is selectable, the Embed Text export is the next thing to try.

## From a live text pdf table to rows in Excel

PDFTrail is my app. It takes the other route. A page with no text layer gets OCR on your Mac, and then the table is built from the position of the recognized text: which fragments share a row, where the column boundaries fall. Nothing is uploaded and no account is needed.

1. Click Open PDF and select the scanned file in the dialog. Select several files for a batch.
2. Choose the formats you want. For a table, tick Excel. Press Convert.
3. When the run ends, go through Table Review page by page. It shows the table PDFTrail found beside the page it came from. It opens by itself when a page's tables were partly read or not read.
4. If a table is wrong, open the grid editor. Nudge the lines, put in any that are missing, or mark where the table sits. Test the new grid, then keep it.
5. Press Accept and re-export to write the files again. That uses no free export.

{{figure}}

Version 1.3.0 also changed how a scan is read. It keeps more of the words and drops repeated words. Some scanners add a hidden text layer, and PDFTrail checks that layer and reads the page again when its own reading is better.

## What this route still gets wrong

OCR is good but not infallible, so the digits are where I look. Pick a handful of figures from the table and compare each with the page. A wrong digit looks exactly like a right one in a spreadsheet.

Finding a table is a separate decision from reading characters, and it can fail in its own way. An early version of the engine invented 26 tables on pages that were pure scanner noise. It reports none there now. The rule I took from that is that a fabricated table is worse than a missed one. If Table Review shows a table on a page that has none, treat it as a defect and do not trust that table.

For the spreadsheet route on scans, start with the [scanned PDF to Excel guide](/blog/scanned-pdf-to-excel-mac/). One document type gets its own walk-through in the [scanned bank statement guide](/blog/scanned-bank-statement-to-excel-mac/). For what OCR can and cannot recover, read [teaching the engine to read bad scans](/blog/teaching-the-engine-to-read-bad-scans/).

## Back to the Option key

Apple's tip is a good one. It gets you a single column from a page that already holds text. A scan is a different case, and a whole table is a bigger job than a column.

Pick the tool for the size of the job. One number, Live Text. One table, anything that shows you the rows.
