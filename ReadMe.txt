How to Use:
		1. Select Blank ScanItem: Enter an Item
		2. Item ID

Setup:
		1. Enable Macros
		
		Install Barcode 39 font (File Included)
			1. Downlaod Barcode Font demo. Soft Code 39 (Demo)
				https://www.softmatic.com/excel/manual.html
			2. Unzip zip file Barcode-AddIn-Fonts-Excel-365-Demo.zip
			3. Navigate to Fonts folder Right click and Install to Windows
		Adding Images
			1. add images to Resources/Items
			2. make sure images are 512 X 512 px
			3. under sheets Items select the cell where you wish to add image click "Add Image"


Licenses:
Code 39 Barcode Font $49.95
	https://www.softmatic.com/excel/manual.html




Development Version Logs:
__________________________________________
Finishing up: Clear any unwanted Message boxes, MsgBox
Finishing Up: Confirm Any code from buttons isn't running more then need be when spam clicking.

Feature: POS Scrollable Receipt window

Todo: Add total price to Sales header
Bug: POS When Cell color red is below item list its not cleared. clear the entire column K:N On change clor before applying Color

Selection: Sheet3 Conditional Formatting Home>Style
	When selection change row color A:G to blue like POS and back to yellow else

Feature: add frese panes to Sheet 3


Bug: Adding Item Locks used cells
Bug: On "Next" Cash should be default on cell I6
Bug: Icons and buttons not locked.


UX&Bug: When entering payment and you dont hit enter, clicking preview dissables cell on escape. When cell change should enter and then preview, (auto preview)
Round to cents Every Where Currency Regulations
	=ROUND(I3 * 0.1, 2)
--------------------Beyond Basic POS
Feature: Receipt numbers should not roll over when exporting. continue Receipt numbers. 
 Item count of 999,999
Feature: Create Custom Item and price to Items WorkSheet, while in POS sheet.
Feature: Image location should search worksheet location address of containing folder called Image or image under resources. to not have the full File directory name.
Feature: LogIn As, admin access needed
Feature: Load reciept by number
Feature: double click
	Receipt Item Clicked jump to Scan Item E10:F10
Feature: LogIn As, admin access needed
Feature: ?? Payment numbers fill from cents to dollars
Feature: security, Log who tried to unlock soft lock when canceld or failed attempts
Feature: Button Jump to Items Sheet to see the List of items
Feature: Seperate all sheets for version control. POS, Items, Sales.
	On Open, search for needed files if it doesn't exist create it.
	Item sheet requirements
		Create xcel file and name it Items
		Cell Range A1:E1 Merge and align Center, value = "Items"
		cell A2 value = Item ID, B2 value = Item Name, C2 value = Item Description, D2 value = Price, E2 value = Image
		Cell Range A1:E2
			 Align center
			 color light green
			 Boarder All
		Cell Range A3:N9999
			Align Center
		Cell Range B3:N9999
			Align left
		Cell Range C3:N9999
			Align Left
		Cell Range D3:N9999
			Align Center
			
	Sales Sheet Requirments
		Create xcel file and name it Sales

Feature: Create a Cashier Log in - with their own Password, also they must enter their password twice once for initial and the second to confirm the initial password.
Feature: Password Encription and Decription for Validators


Development Change Log:
__________________________________________
-------------------------UnStaged Commit:
Items Sheet:
	Feature: hide full directory on Item sheets
	Create an open directory
	Set cell value with file name
UX: Sales Formatting should be Recept number Date, Cashier then Recept Total.
		After that its the list of items
Feature: Item Sheed Keep header always visiable when scrolling down
Feature: Sheet 1, must be able to scroll down the receipt while keeping the controls stationary.
Feature: open file on Sheet1 (POS)
Todo: make the enire row clickable

-------------------------Staged Commit:
Bug: first item in list is ignored when setting header
Bug: SelectionChange On Cells (E10:F10, I7, F6, F8, J4) Save the cell value as string then clear it. 
	if selection change other then cell cleared past that value back to original cell.
	Create a seperate function called by cells (E10:F10, I7, F6, F8,) and cell J4
	Save value and re enter if cell changed from original cell.
Receitp click on QTY should jump to QTY F8
Receipt Clicked on price Jump to Price F6
Impliment Admin Access
Impiment Edit mode
Bug: Clear button should only clear data fields nothing more
Bug: Adding a Decimal doesn't register
	When empty point registers
Bug: Receipt Number Increments based on Item counting.
	Other bug, Receipt number doesn't update to current reciept When making changes
Fix: If Preview Then select Item, we need to click preview again.
Fix: On Open Must clear all like Next
	Hide Item picutre
	RemoveTotal
	Subtotal
		Tax
		Change
		Total
Bug: Entering Item should clear Item selection. (ClearContents B6)
Bug: When no item is selected, item image price and Qty should be empty
Feature: Admin Password Validator
Fix: Lock Sheet to not allow Edit to items and images, icons, buttons
Bug: Change is Negative in Receipt footer Change: ()
Fix: after removing item return back to E10 for the next item
Bug: Performance, When locking Sheet takes forever to finish. (remove any iterations)
Feature: Worksheet_Change() J4 needs to unlock with Admin password for modification no soft-Lock
Bug: When copying item to sale, copy both the strickthrough and no strickthrough
Bug: Remove Item deleats our formating rules.
Add logic keyboard logic to block modification to locked cells and jump to E10
Bug: CalculateAndUpdateTotal is not counting QTY
Bug: Admin Lock when keyboard Enter, the selection is reselected asking for another password after change
Bug: Receipt Number Refference doesn't update Recept
Next button Seperate functionallity (Next)
Bug: Crossed out items remain crossed out.
Bug: Update CalculateAndUpdateTotal when Removing item.
Bug: When sheet is locked Tax rate cant be changed.
Bug: TaxRate after entering its asking for admin password again.
Bug: When hitting Preview finding last recipt item on column M must unlock M cell past then lock again.
Feature: Impiment Remove items










request:
OK, we are creating the 9999 in the correct location at the end of the list, this indicated that we are able to detect an empty cell at the end of our list. given this logic. we need to add 9999 to that empty cell witch we are doing perfectly before any hidden logic is performed if you look at the code we are setting Me.Cells(i, 1).Value = 9999 after our hide and unhide logic. the order of operation is find the empty cell add 9999, unhide the logic in our case we seem to be using Me.Rows(i).Hidden = toggleState. Then unhide the cells, then after clear the cell with 9999 that we found. right now we are able to find the correct palace to put 9999, and we are deleting the correct cell with our place holder. 9999. just modify the code to follow the order of operations.


If Not toggleState Then
          For i = lastRow To Me.Rows.Count
			If data(i, 1) = "" Then
                  lastRow = i
                  Exit For
			End If
		Next i
	End If
	
toggleState = True
For i = 2 To lastRow
	If Me.Rows(i).Hidden Then
		toggleState = False
		Exit For
	End If
Next i