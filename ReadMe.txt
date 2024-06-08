How to Use:
		1. Select Blank ScanItem: Enter an Item
		2. Item ID

Setup:
		1. Enable Macros

		Install Barcode 39 font
		2. Downlaod Barcode Font demo. Soft Code 39 (Demo)
			https://www.softmatic.com/excel/manual.html
		3. Unzip zip file Barcode-AddIn-Fonts-Excel-365-Demo.zip
		4. Navigate to Fonts folder Right click and Install
		5. 


Licenses:
Code 39 Barcode Font $49.95
https://www.softmatic.com/excel/manual.html


Development notes:
__________________________________________
Bug: Adding a Decimal doesn't register
Bug: Admin Lock when keyboard Enter, the selection is reselected asking for another password after change

Bug: Update CalculateAndUpdateTotal when Removing item.
Bug: Remove Item delets our formating rules.
Bug: Crossed out items remain crossed out.

Bug: Worksheet_Change() J4 needs to unlock with Admin password for modification no soft-Lock

Impliment Admin Access
Impiment Remove items
Impiment Edit mode

Receitp click on QTY should jump to F8
Receipt Item Clicked jump to Scan Item E10:F10
Receipt Price Clicked Jump to Price F6

Round to cents Every Where even before retrieving price from Items List
	=ROUND(I3 * 0.1, 2)
	
Next button Seperate functionallity
Clear recept

Load reciept by number

Feature: Payment numbers fill from cents to dollars
Feature: security, Log who tried to unlock soft lock when canceld or failed attempts

Completed
__________________________________________
Bug: CalculateAndUpdateTotal is not counting QTY
Add logic keyboard logic to block modification to locked cells and jump to E10