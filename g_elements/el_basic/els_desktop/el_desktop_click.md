# Mouse click

![](<../../../.gitbook/assets/0 (79).png>)

Element mouse-clicking a selected control element. The component works correctly only inside the Connect to an Application container.

![](<../../../.gitbook/assets/1 (67).png>)

Properties

&#x20;\- Search template: \[String] Control element search template

&#x20;\- Element: \[LTools.Desktop.Model.DUIControl] Reference to a control element

&#x20;\- Coordinates: \[System.Drawing.Rectangle] Cursor click coordinates

&#x20;\- Keyboard key

&#x20;\- Mouse key

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search temaplate + Mouse click + Keyboard
app.Click("{\"Name\":\"Hide\",\"AutomationID\":\"btnVanish\",\"ClassName\":\"Button\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", 
		LTools.Desktop.Model.MouseButtons.BUTTON_LEFT, LTools.Desktop.Model.KeyboardKeys.CTRL, 20000);
//Component link
LTools.Desktop.Model.DUIControl el = app.FindElement("{\"Name\":\"Hide\",\"AutomationID\":\"btnVanish\",\"ClassName\":\"Button\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
app.Click(el);
//Coordinates
app.Click(new System.Drawing.Rectangle(100, 150, 0, 0));

Python
app = LTools.Desktop.DesktopApp.Init(wf, None, "Test_*", 20000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
#Search temaplate + Mouse click + Keyboard
app.Click("{\"Name\":\"Hide\",\"AutomationID\":\"btnVanish\",\"ClassName\":\"Button\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", 
		LTools.Desktop.Model.MouseButtons.BUTTON_LEFT, LTools.Desktop.Model.KeyboardKeys.CTRL, 20000)
#Component link
el = app.FindElement("{\"Name\":\"Hide\",\"AutomationID\":\"btnVanish\",\"ClassName\":\"Button\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}")
app.Click(el)
#Coordinates
app.Click(System.Drawing.Rectangle(100, 150, 0, 0))

JavaScript
var app = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search temaplate + Mouse click + Keyboard
app.Click("{\"Name\":\"Hide\",\"AutomationID\":\"btnVanish\",\"ClassName\":\"Button\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", 
	_lib.LTools.Desktop.Model.MouseButtons.BUTTON_LEFT, _lib.LTools.Desktop.Model.KeyboardKeys.CTRL, 20000);
//Component link
var el = app.FindElement("{\"Name\":\"Hide\",\"AutomationID\":\"btnVanish\",\"ClassName\":\"Button\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
app.Click(el);
//Coordinates
app.Click(new _lib.System.Drawing.Rectangle(100, 150, 0, 0));
```
