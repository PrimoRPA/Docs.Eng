# Read table

![](<../../../.gitbook/assets/0 (109).png>)

Element reading a tabular control element. The component works correctly only inside the Connect to an Application container.

![](<../../../.gitbook/assets/1 (84).png>)

Properties

&#x20; \- Search pattern: \[String] Control search pattern

&#x20;\- Control: \[LTools.Desktop.Model.DUIControl] Control reference

&#x20;\- Variable\*: \[LTools.Desktop.Model.UIDataTable] Variable for storing table reading results

&#x20;\- Time-out\*: \[Int32] Element finish max time (ms)

LTools.Desktop.Model.UIDataTable - Properties:

&#x20;\- RowCount: \[Int32] Row count

&#x20;\- ColumnCount: \[Int32] Column count

&#x20;\- Headers: \[List] Column headers

&#x20;\- Data: \[List>] Table data

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search pattern
LTools.Desktop.Model.UIDataTable tbl = app.ReadDataGrid("{\"Name\":\"\",\"AutomationID\":\"dtgrdSample\",\"ClassName\":\"DataGrid\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
//Component link
LTools.Desktop.Model.DUIControl el = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"dtgrdSample\",\"ClassName\":\"DataGrid\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
tbl = app.ReadDataGrid(el);
foreach (var r in tbl.Data)
	foreach (var c in r)
		LTools.Workflow.PrimoApp.AddToLog(wf, c);

Python
app = LTools.Desktop.DesktopApp.Init(wf, None, "Test_*", 20000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
#Search pattern
tbl = app.ReadDataGrid("{\"Name\":\"\",\"AutomationID\":\"dtgrdSample\",\"ClassName\":\"DataGrid\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}")
#Component link
el = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"dtgrdSample\",\"ClassName\":\"DataGrid\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}")
tbl = app.ReadDataGrid(el)
for r in tbl.Data:
	for c in r:
		LTools.Workflow.PrimoApp.AddToLog(wf, c)
		
JavaScript
var app = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search pattern
var tbl = app.ReadDataGrid("{\"Name\":\"\",\"AutomationID\":\"dtgrdSample\",\"ClassName\":\"DataGrid\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
//Component link
var el = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"dtgrdSample\",\"ClassName\":\"DataGrid\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
tbl = app.ReadDataGrid(el);
for (var i = 0; i < tbl.Data.Count; i++)
	for (var j = 0; j < tbl.Data[i].Count; j++)
		_lib.LTools.Workflow.PrimoApp.AddToLog(wf, tbl.Data[i][j]);
```
