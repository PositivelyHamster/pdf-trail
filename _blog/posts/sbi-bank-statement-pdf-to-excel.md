---
title: SBI Bank Statement PDF to Excel on Mac
description: Getting an SBI bank statement PDF to Excel on a Mac without uploading it: what the file really contains, four steps, and the two checks I never skip.
date: 2026-09-24
time: 18:00
kicker: Field guide
pillar: P1
primary_keyword: sbi bank statement pdf to excel
figure: 01_table_review.jpg
figure_alt: Reviewing a detected table from an SBI bank statement PDF to Excel conversion in PDFTrail on macOS before export
figure_caption: The review screen. This is where the statement stops being a picture and becomes rows you can argue with.
campaign: bl-sbi
status: approved
faq:
  - q: Does this work with a scanned SBI statement?
    a: Yes. Scanned pages have no text layer, so PDFTrail runs OCR on your Mac and shows the table for review before export.
  - q: Do I need an internet connection?
    a: No. Everything runs on your Mac. Nothing leaves the device.
  - q: How much does it cost?
    a: It is free to try, with 10 free Excel exports. The full version is a $24 one-time unlock, no subscription.
  - q: Why not just email the PDF to my accountant?
    a: You can, but that only moves the file. Whoever opens it still needs to pull the transactions into a spreadsheet before they can total or sort them.
  - q: What if the export has fewer rows than my statement?
    a: Check the conversion report first. It lists any page the app skipped, so you know where to look before you assume a row went missing.
---
Page 15 is the one I keep coming back to. It is a bank statement, printed on a dot-matrix printer, spiral bound, and scanned slightly crooked, and the coil of the binding lies right across the middle of the text. It sat inside a 174-page loan application from an Indian public-sector bank. I wanted the transactions in a spreadsheet. The scan wanted nothing to do with me, and neither did any converter I tried on it.

Your SBI statement is almost certainly nicer than that. If you downloaded it from online banking, it is a born-digital PDF, and getting an SBI bank statement PDF to Excel is a short job once you know what the file is. If a branch printed it and someone scanned it, you are closer to my page 15, and the job is still doable. It just needs one extra look.

## What an SBI statement PDF actually contains

Here is the thing nobody tells you. A PDF has no table in it. It has short runs of text, each pinned to coordinates: this date at this x and y, this amount a little to the right. The rows you see are an optical effect of good alignment. So when you select the whole page in Preview and paste it into Excel, Excel receives a stream of fragments with no idea which ones belonged together, and it does the only thing it can. One long line.

Retyping avoids that, at the cost of an evening and a transposed digit you find in March.

The converter sites that top the search results avoid it too, at a different cost. They need the file first. I wouldn't send a document with my account number and a year of my spending to a server I can't name, and I don't think you should either. Excel for Mac can't help, by the way. The "From PDF" import that Windows users get in Power Query was never built for the Mac, as Microsoft's own answers forum [confirms](https://learn.microsoft.com/en-us/answers/questions/5116197). People keep looking for that button anyway.

PDFTrail is my app. I built it to read Indian annual reports into a language model without uploading them, and a bank statement turned out to be the same problem in a smaller envelope. It reads the text runs and their positions straight out of the file, works out which runs sit on one line and where the columns break, and hands you the rows before it writes anything. Nothing leaves the Mac. There's no account, and it works with Wi-Fi off.

## The four steps, SBI bank statement PDF to Excel

1. Drop the statement PDF into PDFTrail.
2. Wait for the read. A downloaded statement has a text layer, so the text is read directly, no OCR. A scanned one has only pixels, so OCR runs on the Mac first.
3. Look at the review screen. Check that dates sit in the date column and amounts in the amount column. Count the rows against the printed statement.
4. Export to .xlsx.

{{figure}}

For twelve months of statements, drop the folder instead of one file. Batch conversion runs the lot, one sheet per statement, and you review each one as it comes up. The review is the part I'd never automate away, because it's the only moment you're looking at the numbers with the source page next to them.

## The two checks I never skip

The first is the row count. If the statement shows 87 transactions and the sheet has 84, something was missed, and the conversion report will tell you which page. It lists every page the app skipped and every cell it flagged, so you're not hunting.

The second is the balance column. Walk down it. Each balance should equal the one above it, plus the credit or minus the debit on that row. Where that chain breaks, you've found either a misread digit or a missing row, and you've found it in ten seconds instead of at tax time. On a scanned statement, DIGITGUARD marks digits it isn't sure about so you look there first. It marks them. It doesn't change them.

I can't tell you the exact column order of your statement, because SBI's layouts differ by account type and change over time, and I don't have yours in front of me. Date, narration, debit, credit, balance is the usual shape. Some add a reference number. The review screen exists so you check your file, not my description of it.

## Back to page 15

The coil across the text beat the engine. It found no usable table on that page, and it said so, which is the correct answer. A fabricated table is worse than a missed one, and it took 26 invented tables on pure scanner noise, early on, to make that rule stick. So in the current version you draw the grid yourself on a page like that, drag the column lines to where the coil isn't, and export. The rest of the form went through without me.

Your SBI statement will not have a spiral coil across it. It'll take the four steps, and then the two checks, and then it's a spreadsheet you can pivot by month or hand to whoever asked. If you have statements from other banks in the same folder, the [general bank statement guide](/blog/convert-bank-statement-pdf-to-excel-mac/) covers the differences, and the [PDF to Excel guide](/blog/pdf-to-excel-mac/) is the wider map.

Check the balances anyway. It's your money, and it takes ten seconds.
