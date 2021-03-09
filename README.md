# veritcal-bar-chart
## Add this code in the google sheet apps script 

```

if (e.parameter.method == "vertical") {
    var sheet = SpreadsheetApp.getActiveSpreadsheet().getSheetByName("vertical-bar-chart");
    var data = sheet.getDataRange().getValues();
    Logger.log(JSON.stringify(data));
    return ContentService
      .createTextOutput(e.parameter.callback + "(" + JSON.stringify(data) + ")")
      .setMimeType(ContentService.MimeType.JAVASCRIPT);
  }

  ```