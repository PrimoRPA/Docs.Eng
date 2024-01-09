# Read range

A component for getting data from a Google Sheets cell range. 

![](<../../../.gitbook/assets/image (184).png>)

| Property                | Type                                                                                       | Description                                                                            |
| ----------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| Range                   | String                                                                                     | Cell reading range (A1:D12). If nothing is specified, current selection will be used as the range. |
| Sheet name              | String                                                                                     | Sheet name                                                                             |
| Variable (text)         | List\<List\<string>>                                                                       | Variable that stores reading results with text values                                  |
| Variable (info)         | List\<List<[LTools.Office.Model.ExcelCellInfo](../els\_excel/datatypes/excelcellinfo.md)>> | Variable that stores reading results with cell info                                    |
| Variable (table)        | System.Data.DataTable                                                                      | Variable that stores reading results                                                   |
| Headers row             | bool                                                                                       | First row contains headers (for a table)                                               |



## ExcelCellInfo

LTools.Office.Model.ExcelCellInfo

| Property         | Type                                          | Description                                       |
| ---------------- | --------------------------------------------- | ------------------------------------------------- |
| Value            | [LTools.Office.Model.CellValue](cellvalue.md) | Cell value                                        |
| TextValue        | String                                        | Cell text value                                   |
| BackroundColor   | [System.Drawing.Color](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.color?view=net-8.0) | Cell background color |
| FontColor        | System.Drawing.Color                          | Cell font color                                   |
| BorderType       | LTools.Office.Model.ExcelBorderTypes?         | Cell border type                                  |
| CustomBorderType | LTools.Office.Model.ExcelCustomBorderTypes\[] | Cell border type for ExcelBorderTypes.Custom      |
| Height           | [double?](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | Row height (determined by the first cell) |

Symbol ? in the data type means that the value can be null.

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.Office.GoogleSheetsApp app = LTools.Office.GoogleSheetsApp.Init(wf, @"Token file path", @"Spreadsheet ID");
//String array
List<List<string>> data = app.ReadRange("A1:B1", "Sheet1");
//Cell info array
List<List<LTools.Office.Model.ExcelCellInfo>> data2 = app.ReadRangeInfo("A1:B1", "Sheet1");
//Table
System.Data.DataTable data3 = app.ReadRangeTable("A1:B1", "Sheet1");
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.Office.GoogleSheetsApp.Init(wf, "Token file path", "Spreadsheet ID")
#String array
data = app.ReadRange("A1:B1", "Sheet1")
#Cell info array
data2 = app.ReadRangeInfo("A1:B1", "Sheet1")
#Table
data3 = app.ReadRangeTable("A1:B1", "Sheet1")
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
let app = _lib.LTools.Office.GoogleSheetsApp.Init(wf, "Token file path", "Spreadsheet ID");
//String array
var data = app.ReadRange("A1:B1", "Sheet1");
//Cell info array
var data2 = app.ReadRangeInfo("A1:B1", "Sheet1");
//Table
var data3 = app.ReadRangeTable("A1:B1", "Sheet1");
```
{% endtab %}
{% endtabs %}
