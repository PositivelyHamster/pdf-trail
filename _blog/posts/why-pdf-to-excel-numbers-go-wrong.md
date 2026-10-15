---
title: Why PDF to Excel Gets Numbers Wrong, and How to Catch It
description: A pdf to excel wrong numbers slip can hide in a clean column of amounts. Why it happens, and the checks that catch it fast.
date: 2026-10-15
time: 09:00
kicker: Engine notes
pillar: P6
primary_keyword: pdf to excel wrong numbers
figure: 08_table_review_130.jpg
figure_alt: Table Review grid editor on a Mac: a sales table with grid lines over its page, the engine's output beside it, a way to catch a pdf to excel wrong numbers slip
figure_caption: Table Review after the conversion: the page, what the engine wrote for it, and the grid you are trying.
campaign: bl-wrongnums
status: approved
faq:
  - q: Why does a PDF to Excel conversion get one number wrong?
    a: A wrong number usually starts at one of a few points, a misread character on a scan, a table boundary that shifts a number sideways, or a format Excel reads as text instead of a value.
  - q: Can Excel skip a number in a SUM formula without showing an error?
    a: Yes. If a cell holds a number stored as text, SUM ignores it, and the total comes out short with no warning on the sheet.
  - q: Does a downloaded bank statement carry the same risk as a scanned one?
    a: It avoids the scanning cause entirely, since the text is read straight from the file on your Mac. A table-boundary or text-formatting slip can still happen, so the check is worth doing anyway.
  - q: Where do I check a converted number against the source page?
    a: In Table Review, which runs on your Mac after the conversion and shows each detected table next to the page it came from.
  - q: Why do brackets around an amount cause a problem after conversion?
    a: Some spreadsheets read a bracketed amount as text rather than a negative number, so it can drop out of a sum until it is converted back to a value.
---
Open a spreadsheet that came out of a PDF and scroll down a column of amounts. Every cell lines up. Every decimal sits where it should. One number in that column is wrong, and nothing on the screen tells you which one. A bad conversion does not look bad. It looks exactly like a good one, right up until you add the column and the total is off.

The wrong number rarely comes from one glitch. It shows up at a handful of different points in the process, and each point leaves a different kind of mistake behind. Knowing where a mistake is usually born tells you where to look for it, instead of rereading the whole sheet.

## Where OCR misreads a character on a scan

A scanned page is not text. It is a picture of text, and something on your Mac has to work out the letters from the shape of the ink. Most of the time that is easy. A worn photocopy, a faint fax, or a page scanned at an angle makes it harder. A few characters are close enough in shape to trade places: an 8 for a 3, a 1 for a 7, a 0 for the letter O, a 5 for an S. The reading comes back looking right and is not, and the wrong character sits in the cell looking exactly like the right one would have.

A downloaded statement, an emailed invoice, anything produced by software rather than a scanner, skips this cause completely. The text is read directly from the file, no OCR guessing, because the characters and their positions are already stored on the page. The [scanned PDF to Excel guide](/blog/scanned-pdf-to-excel-mac/) covers what that OCR pass looks like end to end, and what a page with no usable text looks like when the engine gives up rather than guess.

## Where the table structure shifts a number

Even a correctly read character can end up in the wrong place. Turning a page of positioned text into rows and columns means deciding where one row ends and the next begins, and where one column stops and its neighbour starts. Get a boundary wrong, on a tight column or across a page break, and a correct number lands one column over, or two rows fuse into one. This is not a misread digit. It is a right digit in the wrong house, and it is easy to miss, because the number itself was never wrong. Only its address was.

The mechanism behind that reconstruction, why a PDF has no table stored in it at all, is the subject of the [table extraction guide](/blog/how-pdf-table-extraction-works/). I have also written about [what happens when a page is too far gone to read at all](/blog/teaching-the-engine-to-read-bad-scans/). It is the far end of the same problem, a grid built from noise instead of a real row.

## Where the spreadsheet decides a number is text

The third failure point is not in the PDF. It sits in the spreadsheet, after the file has already opened correctly. A thousands separator, a currency symbol, a trailing Dr or Cr, or a negative amount shown in brackets can make a program treat a cell as text rather than a number. The digits look fine. A SUM formula run over that column quietly skips the cell, and the total comes out short by exactly that one amount, with no error on the sheet.

Microsoft's support page on [numbers stored as text](https://support.microsoft.com/en-us/excel/convert-numbers-stored-as-text-to-numbers-in-excel) walks through the fix. Convert the affected cells back to numbers, or run them through a formula that forces the value out of the text. It is worth knowing this happens in any spreadsheet, built from any source, PDF or typed by hand. A converted file just hands you a whole column of these cells at once, arriving in one paste instead of one entry at a time.

## The checks that take seconds

None of these failure points need a forensic pass over the sheet. A few checks catch almost all of them, and each one is quick.

1. Sum the column and compare it with the printed total on the source document.
2. Walk the running balance down the page, if the document has one, checking that each line still equals the one above it plus or minus that row.
3. Sort the column and look at the highest and lowest values. A misread character can produce an amount that is off by a whole order of magnitude.
4. Compare any number that looks odd against the source page, in Table Review, which shows both side by side.

{{figure}}

PDFTrail writes the files first. Then Table Review shows each detected table next to the scanned or downloaded page it came from, and it opens by itself when a page needs a look. Checking one odd number against the source takes a glance, not a recount of the whole column. If a table is wrong, drag the grid lines into place in the grid editor, then click Accept and re-export. PDFTrail is my app, and I built this step because I would rather you catch a wrong number in seconds than find it in a total that has already gone out the door.

## Back to the column

Back to the column at the top of this page. One of those numbers is wrong. Now you know where a mistake like that is usually born: a scan an OCR pass misread, a boundary the reconstruction stepped over, or a format the spreadsheet decided was text and not a value. Two of those causes have nothing to do with scanning, and they will happen to a column typed in by hand as well.

A born-digital PDF removes the scanning cause outright, since there was never a scan to misread in the first place. The other two still deserve a look, however the file arrived on your Mac. Sum the column. It takes seconds, and it is your money sitting in that one cell.
