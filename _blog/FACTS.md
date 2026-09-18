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
- Free tier: 10 free exports per format for Markdown, Word (.docx), and Excel (.xlsx). Plain text (.txt) and JSON export are free with no limit.
- Full version: $24, one-time in-app purchase, "Unlock Full Version". No subscription. No account.

## What it does

- Converts PDFs on your Mac to Excel (.xlsx), Word (.docx), Markdown (.md), CSV, JSON, and plain text.
- Everything runs on the Mac. Nothing is uploaded. No account, no sign-up, no internet connection needed to convert.
- Born-digital PDFs (files that were produced by software, such as a statement downloaded from a bank website): the text is read directly from the file, with the position of every character. No OCR guessing. This is the honest hook; use these words.
- Scanned PDFs (photocopies, faxes, phone photos saved as PDF, any page with no text layer): the app runs OCR on the Mac. OCR is good but not infallible. The app shows the detected tables in a Table Review step before anything is exported, so you check the numbers first.
- Tables: the app reconstructs tables from the geometry of the positioned text (which fragments share a row, where the column boundaries fall). Rows and columns come out intact in the export.
- Conversion report: after a conversion, the app lists pages it skipped and cells it flagged, so nothing is dropped silently.
- DIGITGUARD: a numeric audit that flags suspicious digits in scanned tables for the reader to check. It flags; it never silently "corrects" a number.
- Batch conversion: drop a folder of PDFs and convert them in one pass.
- Images inside text PDFs: OCR also runs on images embedded in an otherwise born-digital PDF (since version 1.2).
- Version 1.2 shipped on 2026-08-26 and is the current version. Release notes: https://pdftrail.app/blog/pdftrail-1-2/

## Facts about other tools (allowed, with the citation)

- Excel for Mac has no "From PDF" (Power Query) connector. That connector is Windows-only. Cite: https://learn.microsoft.com/en-us/answers/questions/5116197 and https://support.microsoft.com/en-us/office/power-query-data-sources-in-excel-versions-e9332067-8e49-46fc-97ff-f2e1bfa0cb16
- Excel and Numbers cannot open a PDF as a table. Word can open a PDF and tries to convert it; it is built for prose and usually mangles tables.
- Preview (macOS) copy-paste from a PDF loses column structure because a PDF stores positioned text fragments, not a table.
- Tabula is a free open-source tool that needs Java. Cite: https://tabula.technology/
- camelot and pdfplumber are Python libraries; they need a Python setup and code. Cite: https://camelot-py.readthedocs.io/ and https://github.com/jsvine/pdfplumber
- Adobe Acrobat (paid subscription) can export PDF to Excel; Adobe's cloud services process files on Adobe servers for some features. Cite Adobe's own help page and do not characterise beyond what it says. UNVERIFIED: https://helpx.adobe.com/acrobat/using/convert-pdf-excel.html returned 403 to an automated fetch on 2026-09-18; a writer must open it in a browser and confirm the page before citing it.
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
