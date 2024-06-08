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
UIUX: Call event when Quanity is selected and clear image, we cant enter QTY before adding item must find a solution for fast scanning either after scan. Clear cell before entering numeric values. allow numeric only.

Bug: When copying item to sale, copy both the strickthrough and no strickthrough

Bug: Receipt Number Increments based on Item counting.
	Other bug, Receipt number doesn't update to current reciept When making changes

Bug: Adding a Decimal doesn't register
	When empty point registers
	
Bug: Performance, When locking Sheet takes foever to finish. (remove any itterations)
	
Feature: Worksheet_Change() J4 needs to unlock with Admin password for modification no soft-Lock

Impliment Admin Access
Impiment Edit mode


Receitp click on QTY should jump to F8
Receipt Price Clicked Jump to Price F6

Bug: Focus On non editable cells must clear on focus (E10:F10, I7, F6, F8, J4)

Round to cents Every Where even before retrieving price from Items List
	=ROUND(I3 * 0.1, 2)
	
Clear recept

Feature: Load reciept by number

Feature: double click
	Receipt Item Clicked jump to Scan Item E10:F10
	
Feature: ?? Payment numbers fill from cents to dollars
Feature: security, Log who tried to unlock soft lock when canceld or failed attempts
Feature: Button Jump to Items Sheet to see the List of items


Completed
__________________________________________
						UnStaged Commit:
Bug: Receipt Number Refference doesn't update Recept
Next button Seperate functionallity (Next)
Bug: Crossed out items remain crossed out.
Bug: Update CalculateAndUpdateTotal when Removing item.
Bug: When sheet is locked Tax rate cant be changed.
Bug: TaxRate after entering its asking for admin password again.
Bug: When hitting Preview finding last recipt item on column M must unlock M cell past then lock again.
Feature: Impiment Remove items

						Staged Commit:
Bug: Remove Item deleats our formating rules.
Add logic keyboard logic to block modification to locked cells and jump to E10
Bug: CalculateAndUpdateTotal is not counting QTY
Bug: Admin Lock when keyboard Enter, the selection is reselected asking for another password after change