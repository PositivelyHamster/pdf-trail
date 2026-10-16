---
title: Axis, Kotak, and Other Indian Bank Statements to Excel
description: Bank statement PDF to Excel India guide, combining Axis, Kotak, and other statements into one sheet, with checks before you merge.
date: 2026-10-16
time: 09:00
kicker: Field guide
pillar: P1
primary_keyword: bank statement pdf to excel india
figure: 09_cross_page_tables_130.jpg
figure_alt: A three-page PDF table beside the one Excel table PDFTrail wrote from it, with Index and Extracted sheet tabs, for a bank statement pdf to excel india folder
figure_caption: A table that runs over three PDF pages, written as one Excel table, with the Index and Extracted tabs below it.
campaign: bl-inbank
status: approved
faq:
  - q: Can PDFTrail combine statements from Axis, Kotak, and other banks into one file?
    a: Yes. Turn on "Combine into one file per format" and every table lands in one workbook on your Mac, with an Index sheet that shows which file each table came from. Merging the rows into one list is a step you do afterward, once the column names match.
  - q: Do all Indian banks lay out their statements the same way?
    a: No. Column order, column names, and how debit and credit are marked all vary by bank, and the review screen shows what your file actually contains.
  - q: Does this work with a scanned statement from one of the banks in my folder?
    a: Yes. A scan has no text layer, so PDFTrail runs OCR on your Mac. Table Review then lets you check the detected table after the conversion.
  - q: Do I need an internet connection to convert statements from several banks at once?
    a: No. Reading a statement and running OCR both happen on your Mac. Nothing in the folder is uploaded anywhere.
  - q: How much does PDFTrail cost?
    a: It is free to try, with 10 free Excel exports. The full version is a one-time $24 unlock, no subscription.
---
Suppose your downloads folder holds statements from three different banks, because your salary lands in one account, your savings sit in another, and a small side income comes into a third. A search for a bank statement PDF to Excel India guide usually assumes one bank; your folder has three, or four, or five. Every one of those PDFs holds the same kind of table: a date, a narration or description, an amount, a running balance. Almost nothing else about the three files agrees. One bank puts debit and credit in separate columns. Another prints a single signed amount and lets a plus or a minus carry the meaning. One calls the description field "narration"; another calls it "particulars", and a third just calls it "description".

Open each PDF in Preview and paste the page into a spreadsheet, and you get one long column of fragments, not a table, because a PDF never stored a table to begin with. Retype each statement by hand instead, and the work multiplies by however many banks you use, along with the odds of a transposed digit. An upload site asks for the file before it will convert anything, and now you are sending three or four banks' worth of account numbers to a server instead of one.

## What an Indian bank statement PDF actually holds

I don't have your three statements in front of me, so this is the shape, not your exact columns. A downloaded statement is really a scatter of short text pieces, each fixed at its own spot on the page: a date here, an amount somewhere off to the side. The row you see is what your eye does with good alignment, not something the file recorded on its own. Copy that page into a spreadsheet and the fixed spots vanish, so every piece lands in whatever order the file stored it, with nothing left to show which piece sat next to which.

That much is true of any bank's statement, born-digital or not. Layouts on top of it differ because every bank designs and prints its own statement, and none of them checks its column order against anyone else's. Axis, Kotak, and the rest each settle on their own headings, and some change that layout across the years.

PDFTrail is my app. For a downloaded statement, it reads the text and its position straight out of the file, no OCR guessing needed. From there, it figures out on its own which pieces sit on the same line, and where one column ends and the next begins. A scanned or photocopied statement has no text layer, so OCR runs on the Mac first. Either way, the files are written when the conversion ends, and Table Review lets you check each statement's tables. Batch conversion goes through the whole queue in one run, one statement at a time.

## Bank statement PDF to Excel India, one folder at a time

1. Put every statement in one folder, whichever bank sent it and whatever shape its columns are in.
2. Click Open PDF, then open that folder in the dialog and select all its PDFs. Batch conversion goes through each file in turn.
3. Convert to Excel (.xlsx). Each PDF gets read on its own terms: a downloaded statement from its text layer, a scan through on-device OCR first.
4. Check the table PDFTrail found for each statement in Table Review, bank by bank. Table Review opens by itself on a page that needs a look; the toolbar button opens it for the rest. Check that this bank's own columns landed where they should, since the next bank's file may look nothing like it.
5. If a statement's table is wrong, fix its grid in the editor and click Accept and re-export. By default you get one spreadsheet per statement, still carrying that bank's own column order and names.

{{figure}}

## Naming the columns the same way

Each exported sheet keeps the heading its own bank used. That's correct and worth leaving alone until you actually try to combine sheets, because a formula or a pivot table can't tell that "particulars" and "narration" mean the same field. Pick one set of column names you'll use everywhere: date, description, debit, credit, balance, or a single signed amount if you'd rather work that way. Rename the headings on each exported sheet to that set before you copy any rows into a combined file. It's a few clicks per statement, done once per bank, not once per row.

Where a bank splits debit and credit and another doesn't, decide the shared shape first and convert toward it, rather than improvising bank by bank as you go. A single signed-amount column is usually the easier target. A separate debit and credit column can always be turned into one signed number, while going the other way needs a rule for which column a bare number belongs in.

## Checking each bank before you merge

Do this before the sheets get combined, not after, because a mistake is far easier to trace inside one bank's own numbers than after three banks' rows are sitting in one long list. Walk down each statement's balance column on its own sheet. Every balance should equal the one above it, plus that row's credit or minus its debit. Where the chain breaks, you've found a misread digit or a missing row, and you know exactly which bank and which page to open again.

Do the same row count check per bank: compare the number of rows PDFTrail wrote against the transactions the statement itself claims to list, or against a quick count on the printed page. A shortfall almost always sits at a page break inside that one file, so Table Review for that specific statement is where to look first.

Only once each bank's own sheet checks out is it worth merging them. A combined sheet is convenient for a total across accounts, or for a return you're preparing. It's also where an error from one bank hides behind the correct numbers from the other two. Check first, merge second.

## Back to the folder

The folder started as three unrelated PDFs, each with its own idea of a column. It ends as one sheet, with one set of headings, and balances that each add up on their own terms before anything gets merged. Statements from any of these accounts may end up backing a return at some point. The return itself gets filed on the government's own portal at [incometax.gov.in](https://www.incometax.gov.in/), and nothing about reaching that stage needs any of these files to leave your Mac first.

If you'd rather work through one bank before you touch the folder, three guides cover a single statement in more depth: [SBI](/blog/sbi-bank-statement-pdf-to-excel/), [HDFC](/blog/hdfc-bank-statement-pdf-to-excel/), and [ICICI](/blog/icici-bank-statement-pdf-to-excel/).

Three banks, three layouts, one sheet. Check each one before you merge them, and the folder stops fighting you.
