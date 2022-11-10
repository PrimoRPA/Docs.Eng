# Read table

![](<../../../.gitbook/assets/image (233).png>)

Element reading the data of a tabular control element. The component works correctly only inside the Open a Browser or Connect to a Browser container.

![](<../../../.gitbook/assets/1 (39).png>)

Properties

&#x20;\- Search template: \[String] Control element search template

&#x20;\- Element: \[LTools.WebBrowser.Model.IElementInfo] Reference to a control element

&#x20;\- String tag\*: \[String] String element tag

&#x20;\- Column Tag \*: \[String] Column element tag

&#x20;\- Header tag: \[String] Header element tag

&#x20;\- Variable\*: \[LTools.WebBrowser.Model.WebDataTable] Variable that stores table reading results

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search pattern
LTools.WebBrowser.Model.WebDataTable tbl = app.ReadDataGrid("{\"Tag\":\"DIV\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"header-bar\"}]}", "A", "SPAN");
//Component link
LTools.WebBrowser.Model.IElementInfo el = app.FindElement("{\"Tag\":\"DIV\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"header-bar\"}]}");
tbl = app.ReadDataGrid(el, "A", "SPAN");		
foreach (var r in tbl.Data)
	foreach (var c in r)
		LTools.Workflow.PrimoApp.AddToLog(wf, c);	
		
Python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
#Search pattern
tbl = app.ReadDataGrid("{\"Tag\":\"DIV\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"header-bar\"}]}", "A", "SPAN")
#Component link
el = app.FindElement("{\"Tag\":\"DIV\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"header-bar\"}]}")
tbl = app.ReadDataGrid(el, "A", "SPAN")
for r in tbl.Data:
	for c in r:
		LTools.Workflow.PrimoApp.AddToLog(wf, c)
		
JavaScript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search pattern
var tbl = app.ReadDataGrid("{\"Tag\":\"DIV\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"header-bar\"}]}", "A", "SPAN");
//Component link
var el = app.FindElement("{\"Tag\":\"DIV\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"header-bar\"}]}");
tbl = app.ReadDataGrid(el, "A", "SPAN");	
for (var i = 0; i < tbl.Data.Count; i++)
	for (var j = 0; j < tbl.Data[i].Count; j++)
		_lib.LTools.Workflow.PrimoApp.AddToLog(wf, tbl.Data[i][j]);
```
