# Credit due to Excel For Freelancers for the template
How to create a Powerful Point Of Sale Application in Excel
https://www.youtube.com/watch?v=C-jw10s8esw&t=1993s

# How to Use POS Worksheet:

1. Enable Macros (if not already enabled).
2. Set Tax Rate in cell J4.
3. Select a blank Scan Item area (E10:F10).
4. Enter Item ID (refer to the Item Sheet).
5. Select Payment type (automatically moves to cell I7).
6. Enter value above Total.
7. Hit Preview (if no bar-code is visible, scroll to Setup > Install).
8. Print button (scroll to Setup > Print Settings).
9. Next Button: finalizes the transaction, saves, and clears for the next customer.
10. Adding images: scroll to Setup > Adding images to items list.
11. For an in-depth overview of bugs and features added to this Worksheet, feel free to read the `Change_Log.txt` file located in the "Resources/" folder.

## Button Explanations:

### User Interactions:
- Note: On the POS Sheet, clicking a data field will automatically clear it.
- Note: On the Sales Sheet, if the entire list is deleted, the POS Receipt number will start at POS Start Recpt # in cell B8 and requires an Admin Password to change (hit the Edit button).

### Sheet POS Buttons:
- Numeric: works only on Data fields.
- Clear Cell: clears only Data field (indicated by a white Cell).
- Prev: for Previewing Receipt.
- Next: Finalizes Transaction, saves, and clears.
- Lock: locks the entire POS and should remain locked unless editing.
- Edit: Requires an Admin Password and unlocks everything for exiting POS Sheet.
- Remove Item: Requires an Admin Soft lock password to cross out an item from the list.
- Clear All: Requires Admin Password, clears the entire receipt and data fields (does not save to Sales worksheet).
- Payment: not used.

### Sheet Items Buttons:
- Add Image: Opens Resources/Items to find the image by name and places it on the active cell.

### Sheet Sales Buttons:
- Fold All: collapses all receipts based on matching receipt numbers.
- Unfold All: Un-collapses the entire worksheet.
- Receipt Number header: each receipt header is clickable for expand and collapse.
- Note: Each time we complete a transaction at Sheet1 "POS", it will save, format, and collapse here. Don't worry about existing cell colors as they get overwritten once they're being used.

## Setup:

### Install Barcode 39 font (Files Included):
- Note: Might need to buy a license to use commercially (around $50.00). Scroll down to Licenses.
  1. Skip to step 4; SOFTCode39.ttf file is located in Resources/Add-ins.
  2. Download Barcode Font demo, Soft Code 39 (Demo) [here](https://www.softmatic.com/excel/manual.html).
  3. Unzip the zip file Barcode-AddIn-Fonts-Excel-365-Demo.zip.
  4. Navigate to the Fonts folder, right-click and Install to Windows.

### Adding Images:
- Note: Don't delete DefaultNoImage.jpg from Resources/Items.
  1. Add images to Resources/Items.
  2. Make sure images are 512x512 px for better performance (not required).
  3. Supported files: JPEG (.jpg, .jpeg), PNG (.png), GIF (.gif), BMP (.bmp), TIFF (.tif, .tiff), ICO (.ico), EMF (.emf), WMF (.wmf).
  4. Under sheet Items, select the cell where you wish to add an image and click "Add Image".

### Print Settings:
- Note: Auto Print is based on your printer settings.
  1. Navigate to File > Print > Set Printer here.

## Licenses:
- Code 39 Barcode Font: $49.95, [purchase here](https://www.softmatic.com/excel/manual.html).
