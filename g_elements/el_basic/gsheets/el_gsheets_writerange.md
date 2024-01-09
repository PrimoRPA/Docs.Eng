# Write range

Element that writes cells range to Google Sheets spreadsheet.

![](<../../../.gitbook/assets/image (293).png>)


| Property           | Type                 | Description                                    |
| ------------------ | -------------------- | ---------------------------------------------- |
| Range\*            | String               | Cells range (A1:D12)                           |
| Sheet name         | String               | Sheet name                                     |
| Variable (text)    | List\<List\<object>> | Variable that stores cell range text           |

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.Office.GoogleSheetsApp app = LTools.Office.GoogleSheetsApp.Init(wf, @"Token file path", @"Spreadsheet ID");
app.WriteRange(new List<List<object>>() { new List<object>() { "aaa1", "bbb1" } }, "A1:B1", "Sheet1");
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.Office.GoogleSheetsApp.Init(wf, "C:\\Work\\Primo Test Projects\\ttt\\gstoken\\Google.Apis.Auth.OAuth2.Responses.TokenResponse-user", "11QELuPkG1eD5u3Sn-JSQe4PtJqMqK_-yXKhXiuWQSLA") #LTools.Office.GoogleSheetsApp
app.WriteRange(List[List[object]](), "A1:B1", "Sheet1")
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
let host = new _lib.Microsoft.ClearScript.HostFunctions();
let data = host.newObj(_lib.System.Collections.Generic.List(_lib.System.Collections.Generic.List(_lib.System.Object)));

let app = _lib.LTools.Office.GoogleSheetsApp.Init(wf, "Token file path", "Spreadsheet ID");
app.WriteRange(data, "A1:B1", "Sheet1");
```
{% endtab %}
{% endtabs %}
