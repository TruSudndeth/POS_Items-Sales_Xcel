How to Use POS WorkSheet:
		1. Enable Macros (If not already)
		2. Set Tax Rate J4
		3. Select Blank ScanItem: (E10:F10)
		4. Enter Item ID: Look at Item Sheet
		5. Select Payment type (auto Moves to cell I7)
		6. Enter value Above Total
		7. Hit Preview (Note if no bar-code is visible Scroll to Setup > Install)
		8. Print button: (Scroll to Setup > Print Settings)
		9. Next Button: will finalize the transaction Save and clear for next customer.
		10. Adding images scroll to Setup > Adding images to items list.
		11. for an in-depth overview of Bugs and features added to this WorkSheet feel free to read the change_Log.txt file located in "Resources/" folder.
		
Button Explanations:
	User Interactions:
		Note: POS Sheet, we do have a feature for when a data field is clicked it will clear it automatically.
		Note: Sales Sheet, if the entire list is deleted POS Receipt number will start at POS Start Recpt # on cell "B8" and requires Admin Password to change. (Hit button Edit)
		
		
	Sheet POS Buttons:
		Numeric: only works on Data fields
		Clear Cell: will only clear Data field (Indicated by a white Cell)
		Prev: is for Previewing Receipt
		Next: Finalize Transaction save and clear
		Lock: will lock the entire POS and should remain locked unless you wish to edit.
		Edit: Requires an Admin Password and will unlock everything for exiting POS Sheet.
		Remove Item: Requires an Admin Soft lock password to cross out an item from the list.
		Clear All: Requires Admin Password, and will clear the entire reciept and data fields this button will not save to Sales worksheet.
		Payment: is not used
	
	Sheet Items Buttons:
		Add Image: this button will open Resources/Items to find the image by name and place it on the active cell.
		
	
	Sheet Sales Buttons:
		Fold All: will collapse all reciepts based for all matching reciept numbers.
		Unfold All: will Un-collapse the entire worksheet.
		Receipt Number header: each reciept header is clickable for expand and collapse.
		Note: Each time we complete transaction at Sheet1 "POS" it will save, format, and collapse here. Don't worry about existing cell colors it get overwritten once its being used.

Setup:

		Install Barcode 39 font (Files Included)
			Note: might need to buy a license to use commercially ~$50.00 scroll down to Licenses.
			1. Skip to step 4 SOFTCode39.ttf file is located in Resources/Add-ins
			2. Downlaod Barcode Font demo. Soft Code 39 (Demo)
				https://www.softmatic.com/excel/manual.html
			3. Unzip zip file Barcode-AddIn-Fonts-Excel-365-Demo.zip
			4. Navigate to Fonts folder Right click and Install to Windows
			
		Adding Images
			Note: Dont delete DefaultNoIamge.jpg from Resources/Items
			1. Add images to Resources/Items
			2. make sure images are 512 X 512 px for better performance (Not required)
			3. supported files (JPEG (.jpg, .jpeg), PNG (.png), GIF (.gif), BMP (.bmp), TIFF (.tif, .tiff), ICO (.ico), EMF (.emf), WMF (.wmf))
			4. under sheets Items select the cell where you wish to add image click "Add Image"
			
		Print Settings
			Note: Auto Print is based on your printer settings
			1. navigate to File > Print > Set Printer here


Licenses:
Code 39 Barcode Font $49.95
	https://www.softmatic.com/excel/manual.html




