# FACTS.md — the only facts a writer may state about PDFTrail

Copy these facts as written. Do not infer, extend, round, or "improve" them.
If a fact you need is not here, write around it or leave a `[FACT NEEDED: ...]`
marker for the reviewer. Never guess.

## Product

- Name: PDFTrail. App Store listing name: "PDFTrail - PDF Extractor".
- Maker: Arkya Ghosh, an independent developer. Every post is written in the first person by him. Every post must say plainly that PDFTrail is my app (the exact phrase "PDFTrail is my app" or "it's my app" must appear once).
- Platform: macOS 12 or later, Apple Silicon Macs only. Do not mention Intel Macs at all.
- Where to get it: the Mac App Store, https://apps.apple.com/app/id6799649606. This is the ONLY link allowed, and the template inserts it. Never write an App Store link in the body.
- iOS: an iOS app is in development. Never link it, never name a date, never say "coming soon". Best practice: do not mention it.

## Price

- Free to download and try.
- Free tier: 10 free exports per format for Markdown, Word (.docx), and Excel (.xlsx). Plain text (.txt) and JSON export are free with no limit. After the 10 free Excel exports, Excel export keeps working with the first 15 rows of each table. Conversions and on-screen Table Review are unlimited. The sidebar shows how many free exports are left for each format.
- Full version: $24, one-time in-app purchase, "Unlock Full Version". No subscription. No account.

## What it does (version 1.3.0; checked against the app code 2026-10-11)

- Converts PDFs on your Mac to five formats: Excel (.xlsx), Word (.docx), Markdown (.md), JSON, and plain text (.txt). It does NOT export CSV. If a reader needs CSV, say: export to Excel, then save the sheet as CSV in Excel or Numbers, and cite an Apple or Microsoft support page that you verified in this writing batch.
- Everything runs on the Mac. Nothing is uploaded. No account, no sign-up, no internet connection needed to convert.
- Born-digital PDFs (files that were produced by software, such as a statement downloaded from a bank website): the text is read directly from the file, with the position of every character. No OCR guessing. This is the honest hook; use these words.
- Scanned PDFs (photocopies, faxes, phone photos saved as PDF, any page with no text layer): the app runs OCR on the Mac. OCR is good but not infallible, which is why Table Review exists (below).
- Opening files: click "Open PDF" and choose the PDF in the Open dialog. You can choose several PDFs at once in that dialog. After the first file, the button reads "Add PDFs". There is NO drag-and-drop and NO folder picker. Never tell the reader to drop or drag a file or a folder into, onto, or in the app. To convert a folder, open it in the dialog and select all the PDFs in it.
- Batch conversion: every PDF in the queue converts in one run. The queue has no fixed limit.
- Tables: the app reconstructs tables from the geometry of the positioned text (which fragments share a row, where the column boundaries fall). Rows and columns come out intact in the export.
- Tables across pages (new in 1.3.0): when a table continues on the next page, PDFTrail joins the pieces into one table in Excel, Word and Markdown, with one header row. A row cut by the page break becomes one row again.
- Table Review (new in 1.3.0). The order is exactly this:
  1. You convert. PDFTrail writes the export files.
  2. After the conversion, Table Review opens by itself when a page needs a look (a page whose tables were partly read or not read). At any other time you open it with the "Review tables" button in the toolbar.
  3. Table Review shows each table PDFTrail found, page by page, next to the page it came from.
  4. If a table is wrong, open the grid editor on that page. Drag the grid lines into place, add column or row lines, or draw a table region. Try the new grid, then save the fix.
  5. "Accept and re-export" writes the changed files again with your fixes. A re-export uses no free export credits.
  6. You can also open the files as they are, without fixing anything.
  7. Fixes are saved for that PDF and apply again the next time you convert it. You can tell the app to ignore them.
  Never write that the review comes before export, that nothing is written until you check, or that you can skip a table. Correct framing: "check the tables after conversion, before you rely on the file".
- Three themes (new in 1.3.0): Blueprint, Terminal and Field Unit. Change the theme at any time in the sidebar.
- Scan fixes (new in 1.3.0): cleaner text from scanned pages (more words kept, repeated words dropped); PDFTrail checks the hidden text layer that some scanners add and reads the page again when its own reading is better; it reads downloaded circulars that stack two copies of each page under a watermark; on macOS 27 it finds lone single digits that Apple's text recognizer skips and marks them as recovered; it opens fax-compressed PDF pages.
- Images inside text PDFs: OCR also runs on images embedded in an otherwise born-digital PDF (since version 1.2).
- The version on the Mac App Store is 1.3.0, released 2026-10-10 (iTunes lookup API, checked 2026-10-11). Release notes: the 1.3 release post, slug `pdftrail-1-3`, once it is live; until then link nothing. The 1.2 post (https://pdftrail.app/blog/pdftrail-1-2/) is history.
- Describe ONLY what 1.3.0 does. Before each writing batch the reviewer re-checks the live version with:
  `curl -s "https://itunes.apple.com/lookup?id=6799649606" | python3 -c "import json,sys; print(json.load(sys.stdin)['results'][0]['version'])"`

## BUILT BUT NOT SHIPPED (never describe as available; updated 2026-10-11 for 1.3.0)

These do not exist in the version people can download. Do not mention them at all, not even as "coming soon" or "the next version". They move up to "What it does" only after a release that contains them is live on the App Store and the reviewer has checked the app code.

- The conversion report (a list of skipped pages and flagged cells after each run).
- DIGITGUARD, the numeric audit that flags suspicious digits.
- A second OCR engine asked for candidate readings on a doubtful box.
- Shape checks on identification numbers such as GSTIN, PAN or check characters.
- Drag-and-drop of files or folders into the app window (planned for an update).
- CSV export (the app has none).


## Facts about other tools (allowed, with the citation)

- Excel for Mac has no "From PDF" (Power Query) connector. That connector is Windows-only. Cite: https://learn.microsoft.com/en-us/answers/questions/5116197 and https://support.microsoft.com/en-us/office/power-query-data-sources-in-excel-versions-e9332067-8e49-46fc-97ff-f2e1bfa0cb16
- Excel and Numbers cannot open a PDF as a table. Word can open a PDF and tries to convert it; it is built for prose and usually mangles tables.
- Preview (macOS) copy-paste from a PDF loses column structure because a PDF stores positioned text fragments, not a table.
- Tabula is a free open-source tool that needs Java. Cite: https://tabula.technology/
- camelot and pdfplumber are Python libraries; they need a Python setup and code. Cite: https://camelot-py.readthedocs.io/ and https://github.com/jsvine/pdfplumber
- Adobe Acrobat on the desktop converts a PDF to Excel (XLSX) or XML from its Convert menu. Its settings choose one worksheet per table, per page, or for the whole document, set decimal and thousands separators, and turn on text recognition for scanned text. Cite (verified in a browser 2026-09-28): https://helpx.adobe.com/acrobat/desktop/save-export-documents/convert-to-other-formats/pdf-to-excel.html . Do not state Acrobat prices or plan names.
- Adobe's free online PDF to Excel converter says on its own page that "Your file will be securely handled by Adobe servers and deleted unless you sign in to save it." Cite (verified 2026-09-28): https://www.adobe.com/acrobat/online/pdf-to-excel.html . Quote that sentence at most once and do not characterise Adobe beyond it.
- Online converters require you to upload the file to a third-party server. Say this neutrally; name no specific site.
- Google Sheets has no PDF import. Cite: https://support.google.com/docs/answer/40608

## DO NOT CLAIM (unverified or banned)

- Any accuracy number, percentage, or the words "100%". Never "perfect", "flawless", "never makes mistakes".
- Any speed number (seconds per page, pages per minute).
- Password-protected or encrypted PDFs.
- Specific layout details of a bank statement, tax form, or broker note unless the reviewer has supplied a redacted sample. Without a sample, describe the document in generic terms (a transaction table with date, description, debit, credit, balance) and say layouts vary by bank.
- Anything about Apple's developer contract, App Review, or Apple's fees.
- Any comparison claim that a competitor is "worse"; describe what each tool needs (Java, Python, an upload, a subscription) and let the reader decide.
- Handwriting recognition. PDFTrail does not do handwriting.
- Windows or Linux versions. There are none.
- Testimonials, star ratings, download counts, or "thousands of users".
