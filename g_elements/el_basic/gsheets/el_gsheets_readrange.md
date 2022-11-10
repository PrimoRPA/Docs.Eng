# Read range

Component getting data from the Google Sheets cell range. The component works correctly only inside the Excel application container

![](<../../../.gitbook/assets/image (275).png>)

Properties

* Range: \[String] Cell reader range (A1:D12). If nothong is specified, current selection will be used as range
* Sheet name: \[String] Sheet name
* Variable (text): \[List>] Variable for storing reading results
* Variable (info): \[List>] Variable for storing reading results with cell info
* Variable (table): \[System.Data.DataTable] Variable for storing reading results
* Headers row: First row contains headers (for table)

LTools.Office.Model.ExcelCellInfo - Properties:

* Value: \[LTools.Office.Model.CellValue] Cell value
* TextValue: \[String] Cell text value
* BackroundColor: \[System.Drawing.Color] Cell background color
* FontColor: \[System.Drawing.Color] Cell font color
* BorderType: \[LTools.Office.Model.ExcelBorderTypes?] Cell border type
* CustomBorderType: \[LTools.Office.Model.ExcelCustomBorderTypes\[]] Cell border type for ExcelBorderTypes.Custom
* Height: \[double?] Row height (determined by first cell)
