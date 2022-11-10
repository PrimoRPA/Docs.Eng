# Table

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5\_gIkSrRoHNjhwXgix%2F-M5\_p3NpduwAf8xFeA2q%2FSAP\_%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=8d8f8be3-791c-4ea9-b211-45f59fcf755b)

Element which gets reference to UI component Table.

![](../../../.gitbook/assets/SAP\_table.png)

Properties:

Element which gets reference to UI component Table.

Properties:

* Control ID: \[String] Control ID
* Control: \[LTools.SAP.Model.SAPUIItem] Control reference
* Table: \[LTools.SAP.Model.SAPUIGrid] Variable that stores table reference
* Full read: Full table data read including checkboxes, color etc.
* Variable: \[LTools.SAP.Model.SAPUIGrid] Variable to store table reference
* Cells: \[List\<List\<LTools.SAP.Model.SAPUIGridCell>>] Cell values
* Columns: \[List\<LTools.SAP.Model.SAPUIGridColumn>] Table columns info
* Selected rows: \[List\<int>] Selected rows indexes
* Selected cells: \[Dictionary\<int, string>] Selected cells array
* Select rows: \[List\<int>] Rows indexs to select
* Select cells: \[List\<string>] Cells aray to select
* Click: \[Dictionary\<int, string>] Cell click
* Double click: \[Dictionary\<int, string>] Cell double click
* Toolbar button: \[String] Click toolbar button by ID
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)

LTools.SAP.Model.SAPUIGrid:&#x20;

* \[SAPFEWSELib.ISapGridViewTarget] Element - Element reference;&#x20;
* \[String] Id - Element ID;&#x20;
* \[List\<LTools.SAP.Model.SAPUIGridColumn>] Columns - Columns;&#x20;
* \[List\<List\<LTools.SAP.Model.SAPUIGridCell>>] Cells - Cells;&#x20;
* \[List\<int>] SelectedRows - Selected rows indexes;&#x20;
* \[Dictionary\<int, string>] SelectedCells - Selected cells. Index, Column key;&#x20;
* SelectCells(List cells - strings formatted "Row index, Column key" ("1, NAME")) - Select cells;
* SelectRows(List rows - row indexes) - Select rows;&#x20;
* SetCurrentCell(int row - row index, string column - column key) - Select current cell;&#x20;
* ClickCell(int row - row index, string column - column key) - Performs cell click;&#x20;
* DoubleClickCell(int row - row index, string column - column key) - Performs cell double click;&#x20;
* PressToolbarButton(string id - button ID) - Performs click on table toolbar button.

LTools.SAP.Model.SAPUIGridColumn:&#x20;

* \[String] Key - Column key;&#x20;
* \[String] Text - Column text.

LTools.SAP.Model.SAPUIGridCell:&#x20;

* \[int] Row - Row index;&#x20;
* \[String] Column - Column key;&#x20;
* \[String] Text - Cell text;&#x20;
* \[bool] IsChecked - Is cell checkbox checked;&#x20;
* \[int?] Color - Cell color;&#x20;
* \[int?] ListIndex - Selected item index.

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
LTools.SAP.Model.SAPUIGrid tbl = app.Table("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
tbl.SelectRows(new List<int>() { 1 });

Python
app = LTools.SAP.SapApp.Init(wf)
tbl = app.Table("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell")
tbl.SelectRows(List[int]([ 1 ]))

JavaScript
var host = new _lib.Microsoft.ClearScript.HostFunctions();
var app = _lib.LTools.SAP.SapApp.Init(wf);		
var tbl = app.Table("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
var idx = host.newObj(_lib.System.Collections.Generic.List(_lib.System.Int32));
idx.Add(1);
tbl.SelectRows(idx);
```
