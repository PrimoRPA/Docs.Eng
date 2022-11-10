# Mouse click

![](<../../../.gitbook/assets/image (205).png>)

Element that mouse-clicks a selected control element. The component works correctly only inside the Open a Browser or Connect to a Browser container.

![](<../../../.gitbook/assets/1 (30).png>)

Properties

&#x20;\- Search template: \[String] Control element search template

&#x20;\- Element: \[LTools.WebBrowser.Model.IElementInfo] Reference to a control element

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search pattern
app.Click("{\"Tag\":\"BUTTON\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"btn btn-3d-green button-search\"}]}");
//Component link
LTools.WebBrowser.Model.IElementInfo el = app.FindElement("{\"Tag\":\"BUTTON\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"btn btn-3d-green button-search\"}]}");
app.Click(el);

Python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
#Search pattern
app.Click("{\"Tag\":\"BUTTON\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"btn btn-3d-green button-search\"}]}")
#Component link
el = app.FindElement("{\"Tag\":\"BUTTON\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"btn btn-3d-green button-search\"}]}")
app.Click(el)

JavaScript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search pattern
app.Click("{\"Tag\":\"BUTTON\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"btn btn-3d-green button-search\"}]}");
//Component link
var el = app.FindElement("{\"Tag\":\"BUTTON\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"btn btn-3d-green button-search\"}]}");
app.Click(el);
```
