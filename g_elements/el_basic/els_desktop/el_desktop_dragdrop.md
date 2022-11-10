# Drag and drop

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5uGu7ueL\_Hc9cYNrHE%2F-M5uIXeqQAMsvYlCH5IM%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9\_%D1%81%D1%82%D0%BE%D0%BB\_%D0%BF%D0%B5%D1%80%D0%B5%D1%82%D0%B0%D1%81%D0%BA%D0%B8%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=f1555fa4-22b5-4f06-ae75-68631dc9a4a7)

Element to drag n drop control. There can be drag and drop by the search templates, and in this case Search pattern (source and destination) must be specified, or drag and drop by coordinates, in this case Coordinates (source and destination) must be specified.&#x20;

![](<../../../.gitbook/assets/image (328).png>)

Properties

&#x20;\- Search pattern (source): \[String] Source search pattern

&#x20;\- Control (source): \[LTools.Desktop.Model.DUIControl] Source element reference

&#x20;\- Coordinates (source): \[System.Drawing.Rectangle] Source component coordinates

&#x20;\- Search pattern (destination): \[String] Destination search pattern

&#x20;\- Control (destination): \[LTools.Desktop.Model.DUIControl] Destination element reference

&#x20;\- Coordinates (destination): \[System.Drawing.Rectangle] Destination component coordinates

&#x20;\- Time-out\*: \[Int32] Element finish max time (ms)

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search template
app.DragNDrop("{\"Name\":\"Всем привет!\",\"AutomationID\":\"lbl1\",\"ClassName\":\"Text\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}",
		"{\"Name\":\"\",\"AutomationID\":\"txtTarget\",\"ClassName\":\"TextBlock\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}",
		null, null, System.Drawing.Rectangle.Empty, System.Drawing.Rectangle.Empty, 10000);
//Component link
LTools.Desktop.Model.DUIControl el_from = app.FindElement("{\"Name\":\"Всем привет!\",\"AutomationID\":\"lbl1\",\"ClassName\":\"Text\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
LTools.Desktop.Model.DUIControl el_to = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"txtTarget\",\"ClassName\":\"TextBlock\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
app.DragNDrop(null, null, el_from, el_to, System.Drawing.Rectangle.Empty, System.Drawing.Rectangle.Empty, 10000);
//Coordinates
app.DragNDrop(null, null, null, null, new System.Drawing.Rectangle(100, 150, 0, 0), new System.Drawing.Rectangle(200, 250, 0, 0));

Python
app = LTools.Desktop.DesktopApp.Init(wf, None, "Test_*", 20000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
#Search template
app.DragNDrop("{\"Name\":\"Всем привет!\",\"AutomationID\":\"lbl1\",\"ClassName\":\"Text\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}",
	"{\"Name\":\"\",\"AutomationID\":\"txtTarget\",\"ClassName\":\"TextBlock\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}",
	None, None, System.Drawing.Rectangle.Empty, System.Drawing.Rectangle.Empty, 10000)
#Component link
el_from = app.FindElement("{\"Name\":\"Всем привет!\",\"AutomationID\":\"lbl1\",\"ClassName\":\"Text\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}")
el_to = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"txtTarget\",\"ClassName\":\"TextBlock\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}")
app.DragNDrop(None, None, el_from, el_to, System.Drawing.Rectangle.Empty, System.Drawing.Rectangle.Empty, 10000)
#Coordinates
app.DragNDrop(None, None, None, None, System.Drawing.Rectangle(100, 150, 0, 0), System.Drawing.Rectangle(200, 250, 0, 0))
		
JavaScript
var app = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search template
app.DragNDrop("{\"Name\":\"Всем привет!\",\"AutomationID\":\"lbl1\",\"ClassName\":\"Text\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}",
		"{\"Name\":\"\",\"AutomationID\":\"txtTarget\",\"ClassName\":\"TextBlock\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}",
		null, null, _lib.System.Drawing.Rectangle.Empty, _lib.System.Drawing.Rectangle.Empty, 10000);
//Component link
var el_from = app.FindElement("{\"Name\":\"Всем привет!\",\"AutomationID\":\"lbl1\",\"ClassName\":\"Text\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
var el_to = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"txtTarget\",\"ClassName\":\"TextBlock\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
app.DragNDrop(null, null, el_from, el_to, _lib.System.Drawing.Rectangle.Empty, _lib.System.Drawing.Rectangle.Empty, 10000);
//Coordinates
app.DragNDrop(null, null, null, null, new _lib.System.Drawing.Rectangle(100, 150, 0, 0), new _lib.System.Drawing.Rectangle(200, 250, 0, 0));		
```
