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

  ## Add this in the HTML page where you embed the form
  ```
<p>
  <iframe frameborder="0" id="verticalbar" scrolling="no" src="URL-OF-THE-FORM" width="100%"></iframe>
</p>
<script src="/bt_files/2021/form/iframeResizer.min.js"></script>
<script>
  iFrameResize({ log: true }, '#verticalbar')
</script>

  ```