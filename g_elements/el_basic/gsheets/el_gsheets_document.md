# Google Sheets document

This is an element that connects to a Google Sheets spreadsheet.

![](<../../../.gitbook/assets/image (255).png>)


| Property       | Type   | Description                |
| -------------- | ------ | -------------------------- |
| File path\*    | String | Credentials file path      |
| Spreadsheet ID\* | String | Google Sheets spreadsheet ID|

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.Office.GoogleSheetsApp app = LTools.Office.GoogleSheetsApp.Init(wf, @"Token file path", @"Spreadsheet ID");
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.Office.GoogleSheetsApp.Init(wf, "Token file path", "Spreadsheet ID")
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
let app = _lib.LTools.Office.GoogleSheetsApp.Init(wf, "Token file path", "Spreadsheet ID");
```
{% endtab %}
{% endtabs %}
