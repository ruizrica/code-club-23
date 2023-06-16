Google Apps Scripts - Google Sheets
**1. Reading from and writing to cells**

This script reads the value in cell 'A1' and writes that value to cell 'B1' in the active sheet.

```javascript
function readWrite() {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  var value = sheet.getRange('A1').getValue();
  sheet.getRange('B1').setValue(value);
}
```

**2. Creating a custom function**

This script creates a custom function that you can use directly in your Google Sheets, named `MYFUNCTION`. It multiplies the input by 2.

```javascript
function MYFUNCTION(input) {
  return input * 2;
}
```
After saving this script, you can use `=MYFUNCTION(A1)` in your Google Sheets to multiply the value in cell A1 by 2.

**3. Setting cell formatting**

This script sets the background color of cell 'A1' to yellow and text to red.

```javascript
function formatCell() {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  sheet.getRange('A1').setBackground("yellow").setFontColor("red");
}
```

**4. Creating a time-driven trigger**

This script creates a trigger that automatically runs the `readWrite` function every hour.

```javascript
function createTimeDrivenTrigger() {
  ScriptApp.newTrigger('readWrite')
      .timeBased()
      .everyHours(1)
      .create();
}
```
*Make sure to replace the dummy function names and values with your actual values as required. These scripts are basic and meant to be built upon based on your actual needs.
