# Read range

![](<../../../.gitbook/assets/image (63).png>)

Element getting data from the Excel cell range. The component works correctly only inside the Excel application container.

![](<../../../.gitbook/assets/1 (69).png>)



Properties

&#x20;\- Range: \[String] Cell reader range (A1:D12)

&#x20;\- Sheet name: \[String] Sheet name

&#x20;\- Sheet index: \[Int32] Sheet index

&#x20;\- Variable (text): \[List>] Variable for storing reading results

&#x20;\- Variable (info): \[List>] Variable for storing reading results with cell info

LTools.Office.Model.ExcelCellInfo - Properties:

&#x20;\- Value: \[LTools.Office.Model.CellValue] Cell value

&#x20;\- TextValue: \[String] Cell text value

&#x20;\- BackroundColor: \[System.Drawing.Color] Cell background color

LTools.Office.Model.CellValue - Свойства:

\- DateTimeValue: \[DateTime?] Data and time value

&#x20;\- BooleanValue: \[bool?] Boolean value

&#x20;\- NumericValue: \[double?] Numeric value

&#x20;\- TextValue: \[string] Text value

&#x20;\- IsBoolean: \[bool]  boolean value‌ flag

&#x20;\- IsEmpty: \[bool] Empty value‌ flag

&#x20;\- IsText: \[bool] Text value‌ flag

&#x20;\- IsNumeric: \[bool] Numeric value flag

&#x20;\- IsError: \[bool] Error flag‌

&#x20;\- IsDateTime: \[bool] Date-time value flag
