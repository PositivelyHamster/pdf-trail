---
title: Excel for Mac Has No From PDF Import: What to Do Instead
description: Excel for Mac import PDF: Get Data has no From PDF entry. Why the connector stayed Windows-only, and how to get a PDF table onto a Mac anyway.
date: 2026-09-23
time: 18:00
kicker: Comparison
pillar: P5
primary_keyword: excel for mac import pdf
figure: 03_exports_ready.jpg
figure_alt: Exported spreadsheet files, the result of an Excel for Mac import PDF workflow done with PDFTrail
figure_caption: What the Data tab never gave you: a spreadsheet made from the PDF, sitting next to it, ready to open.
campaign: bl-xlmacpq
status: approved
faq:
  - q: Why is there no From PDF option under Get Data on my Mac?
    a: The Power Query PDF connector was built for Excel on Windows and was never added to Excel for Mac, so the menu item you are looking for does not exist there.
  - q: Does Excel for Mac support any other way to import a PDF?
    a: No. Numbers has no PDF import either, and Word can open a PDF but tends to break a table apart because it is built for prose, not grids.
  - q: Is a Mac version of the From PDF connector coming?
    a: Microsoft has not announced one, so the practical move is to work around the gap now rather than wait for it to close.
  - q: Why did an AI assistant tell me the connector exists on my Mac?
    a: Many written answers about Excel describe Windows behavior without noting which platform they mean, and an assistant trained on that text can repeat the same mistake with confidence.
  - q: Can I get a PDF table into Excel on a Mac without uploading the file?
    a: Yes. PDFTrail reads the PDF and writes the table to an Excel file on your Mac, with nothing sent to a server, and it works with Wi-Fi off.
---
Open Excel on a Windows PC, click the Data tab, and Get Data offers an entry called From PDF. Open the same Data tab in Excel for Mac and the entry is not there. Not greyed out, not moved into a submenu you haven't found yet. Absent. Anyone trying an Excel for Mac import PDF workflow for the first time runs into this exact wall. Usually a guide written for Windows sent them looking for a button that was never built for their machine.

Microsoft's own page on Power Query data sources lists every connector against every version of Excel, and the [PDF row carries a note](https://support.microsoft.com/en-us/office/power-query-data-sources-in-excel-versions-e9332067-8e49-46fc-97ff-f2e1bfa0cb16) about needing a Windows-only piece of software underneath it. The tables for Excel on the web and Excel for Mac don't list PDF as a data source at all. It isn't hidden somewhere else on those platforms. It was never shipped there.

## Why the connector stopped at Windows

On Windows, From PDF opens the file, scans the pages, and offers up the tables it can find inside the Power Query editor, ready to load into a sheet. That only works because Windows Excel carries a long list of Power Query connectors built up over years, each written once for that codebase. Excel for Mac runs on a separate codebase with a shorter connector list, and PDF is one of the entries that codebase never received.

Nobody pulled the feature out. It sits on one side of a platform line that was drawn when the connector was first written, and nothing since has moved it.

A PDF itself explains why the import is hard work in the first place. It is not a spreadsheet stored under a different name. A PDF holds short runs of text, each one anchored to a position on the page, with nothing inside the file that labels a row or a column. From PDF has to look at where those runs sit and infer which ones line up. Any tool on any platform that claims to pull a table out of a PDF is doing that same inference, not reading a table that was already there.

## What a Mac user tries first

Without From PDF, the search for a workaround tends to run through the same few stops, and each one runs out of road for a different reason. Preview will let you select a page and copy the text. Paste that into a cell and every fragment lands on its own line, because Preview never knew there were columns to keep together. Numbers has no PDF import of its own. Word opens a PDF and tries to convert it, but Word is built for prose, and it usually pulls a table's grid apart while it works.

Somewhere in that search, a person lands on an online converter and uploads the file, hoping the site gets the columns right. That page now sits on a server nobody at the Mac end controls, which is a bad trade for a bank statement or a client invoice.

Ask an AI assistant instead, and some will describe the very menu path Windows users have. So much written about Excel describes Windows without saying so, and the assistant repeats it without checking your platform. That answer sends a Mac user straight back to the button that was never there.

## The excel for mac import pdf workflow I built

PDFTrail is my app, and it exists because getting a PDF's text onto a Mac spreadsheet needed a tool that assumed macOS from the start rather than porting a Windows habit late. It reads a PDF's own text and the position of each character, then works out which runs share a row and where the column lines fall. It shows you the result before anything is written to disk.

The steps for an excel for mac import pdf task, once you are inside the app, stay short.

1. Drop the PDF into PDFTrail. No upload screen, no account to create first.
2. Let it read the file. A born-digital PDF, one made by software rather than a scanner, already carries its text and the position of every character, so the app reads that directly. No OCR guessing.
3. Check the review screen. Before any file is written, the app shows the rows and columns it found, so you can confirm dates sit under the date heading and totals sit under the totals heading.
4. Export to .xlsx and open it straight in Excel for Mac.

{{figure}}

If the source is a scan instead of a downloaded file, a photocopy or a faxed page with no text layer, the app runs OCR on the Mac first, before it can find any rows. OCR reads an image of a character, not the character itself, and it can misjudge one, which is exactly why the review step comes before export rather than after.

## What to check once the sheet is open

Compare the row count in the exported sheet against what you can count on the source page. If a page produced fewer rows than it should, the conversion report names the page, so you are not rereading the whole document to find it. On a scanned file, DIGITGUARD flags digits it is not confident about; it flags them for you to check, and it never quietly changes a number on its own.

For a folder of statements or invoices rather than one file, batch conversion runs the whole folder in a single pass, and you still review each result before export. That review step is the one place I would not want to automate away, because it is the only moment the numbers and the source page sit next to each other.

The [pillar guide to PDF to Excel on a Mac](/blog/pdf-to-excel-mac/) covers other document types this same way, and the [bank statement walkthrough](/blog/convert-bank-statement-pdf-to-excel-mac/) goes through a financial document end to end.

## Back at the Data tab

Go back to Excel for Mac and click Get Data again, and From PDF is still not there. It was never taken away, so there is nothing to wait for and nothing to file a complaint about. The gap is a fact about the software, not a bug some future update quietly fixes.

What changes is not the menu. It is what you do before you open Excel at all: read the PDF with something built for the platform you are actually on. Then let Excel do what it was always good at, once the rows already exist.
