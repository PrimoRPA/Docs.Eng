# Append range

![](<../../../.gitbook/assets/image (11).png>)

Element that writes data of cell range into Excel&#x20;

![](../../../.gitbook/assets/Excel\_append\_range.png)

Properties

&#x20;\- Range\*: \[String] Cells range (A1:D12)‌

&#x20;\- Sheet name: \[String] Sheet name

&#x20;\- Sheet index: \[Int32] Sheet index

&#x20;\- Overwrite: \[Boolean] Flag of data overwrite

&#x20;\- Variable (текст): \[List\<List\<string>>] Variable to store cell range text

&#x20;\- Variable (information): \[List\<List\<LTools.Office.Model.ExcelCellInfo>>] Variable to store results of cell reading.

LTools.Office.Model.ExcelCellInfo - Properties:

&#x20;\- Value: \[LTools.Office.Model.CellValue] Cell value

&#x20;\- TextValue: \[String] Cell text value

&#x20;\- BackroundColor: \[System.Drawing.Color] Cell background color

LTools.Office.Model.CellValue - Properties:‌

&#x20;\- DateTimeValue: \[DateTime?] Data and time value

&#x20;\- BooleanValue: \[bool?] Boolean value

&#x20;\- NumericValue: \[double?] Numeric value

&#x20;\- TextValue: \[string] Text value

&#x20;\- IsBoolean: \[bool]  boolean value‌ flag

&#x20;\- IsEmpty: \[bool] Empty value‌ flag

&#x20;\- IsText: \[bool] Text value‌ flag

&#x20;\- IsNumeric: \[bool] Numeric value flag

&#x20;\- IsError: \[bool] Error flag‌

&#x20;\- IsDateTime: \[bool] Date-time value flag
