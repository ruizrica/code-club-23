Google Apps Scripts - Google Sheets
<br/>
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

Google Apps Scripts - Google Docs
<br/>
**1. Inserting text**

This script will insert a text at the cursor position.

```javascript
function insertText() {
  var doc = DocumentApp.getActiveDocument();
  var cursor = doc.getCursor();

  if (cursor) {
    var element = cursor.insertText('Hello, world!');
  } else {
    DocumentApp.getUi().alert('Cannot find a cursor in the document.');
  }
}
```

**2. Creating a text table**

This script will create a 2x2 table at the cursor position.

```javascript
function createTable() {
  var doc = DocumentApp.getActiveDocument();
  var cursor = doc.getCursor();

  if (cursor) {
    var element = cursor.insertTable(2, 2);
  } else {
    DocumentApp.getUi().alert('Cannot find a cursor in the document.');
  }
}
```

**3. Applying styles to text**

This script will change the style of the text at the cursor position.

```javascript
function styleText() {
  var doc = DocumentApp.getActiveDocument();
  var cursor = doc.getCursor();

  if (cursor) {
    var element = cursor.insertText('Hello, world!');
    var text = element.asText();
    text.setFontSize(16).setForegroundColor('red').setBold(true);
  } else {
    DocumentApp.getUi().alert('Cannot find a cursor in the document.');
  }
}
```

**4. Replacing text**

This script will replace all instances of a specified string.

```javascript
function replaceText() {
  var doc = DocumentApp.getActiveDocument();
  var body = doc.getBody();
  
  // Replace 'oldText' with 'newText'
  body.replaceText('oldText', 'newText');
}
```

*To run these scripts, you should open your Google Docs document, click on `Extensions -> Apps Script`, and paste these scripts into the Apps Script editor. Replace the placeholder text with the actual text you need.


Google Apps Scripts - Google Slides
<br/>
**1. Creating a new slide**

This script will add a new slide to the active presentation.

```javascript
function createSlide() {
  var presentation = SlidesApp.getActivePresentation();
  var slide = presentation.appendSlide(SlidesApp.PredefinedLayout.BLANK);
}
```

**2. Adding text to a slide**

This script will add a text box to the first slide of the active presentation.

```javascript
function addText() {
  var presentation = SlidesApp.getActivePresentation();
  var slide = presentation.getSlides()[0];
  var shape = slide.insertShape(SlidesApp.ShapeType.TEXT_BOX);
  var textRange = shape.getText();
  textRange.setText("Hello, world!");
}
```

**3. Changing the background color of a slide**

This script will change the background color of the first slide to red.

```javascript
function changeBackgroundColor() {
  var presentation = SlidesApp.getActivePresentation();
  var slide = presentation.getSlides()[0];
  slide.getBackground().setSolidFill('red');
}
```

**4. Creating a shape**

This script will create a rectangle shape in the first slide of the active presentation.

```javascript
function createShape() {
  var presentation = SlidesApp.getActivePresentation();
  var slide = presentation.getSlides()[0];
  var shape = slide.insertShape(SlidesApp.ShapeType.RECTANGLE);
}
```

To run these scripts, you should open your Google Slides presentation, click on `Extensions -> Apps Script`, and paste these scripts into the Apps Script editor. Replace the placeholder values with the actual values you need.

Google Apps Scripts - Google Forms
<br/>
**1. Creating a new form**

This script creates a new form with a given title.

```javascript
function createForm() {
  var form = FormApp.create('My New Form');
  Logger.log('Published URL: ' + form.getPublishedUrl());
  Logger.log('Editor URL: ' + form.getEditUrl());
}
```

**2. Adding a multiple choice question**

This script adds a multiple choice question to an existing form.

```javascript
function addMultipleChoiceQuestion() {
  var form = FormApp.openById('replace_with_your_form_id');
  var item = form.addMultipleChoiceItem();
  item.setTitle('Do you prefer cats or dogs?')
      .setChoices([
          item.createChoice('Cats'),
          item.createChoice('Dogs'),
      ]);
}
```
Replace `'replace_with_your_form_id'` with your actual form's ID.

**3. Sending a form via email**

This script sends the form to an email address.

```javascript
function emailForm() {
  var form = FormApp.openById('replace_with_your_form_id');
  var url = form.getPublishedUrl();
  var email = 'replace_with_your_email_address';
  var subject = 'Please fill out this form';
  var body = 'Please fill out the form at the following URL: ' + url;
  MailApp.sendEmail(email, subject, body);
}
```
Replace `'replace_with_your_form_id'` and `'replace_with_your_email_address'` with your form's ID and recipient's email address respectively.

**4. Setting up a form submit trigger**

This script sets up a trigger that runs a function named `myFunction` whenever a form response is submitted.

```javascript
function createFormSubmitTrigger() {
  var form = FormApp.openById('replace_with_your_form_id');
  ScriptApp.newTrigger('myFunction')
      .forForm(form)
      .onFormSubmit()
      .create();
}
```
Replace `'replace_with_your_form_id'` and `'myFunction'` with your form's ID and the function to be run respectively.

To run these scripts, go to the Apps Script editor from your Google Forms: click on the three-dots menu -> Script editor, and paste these scripts.
