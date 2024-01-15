# Element exists

![](<../../../.gitbook/assets/image (271).png>)

Element that searches for a control element. The component works correctly only inside the Open a Browser or Connect to a Browser container.

![](<../../../.gitbook/assets/1 (31).png>)

Properties

&#x20;\- Search template\*: \[String] Control element search template

&#x20;\- Element: \[LTools.WebBrowser.Model.IElementInfo] Variable for storing a reference to a control element

&#x20;\- Result: \[Boolean] Variable that stores search results

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
LTools.WebBrowser.Model.IElementInfo el = app.FindElement("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}");

Python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
el = app.FindElement("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}")
		
JavaScript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
var el = app.FindElement("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}");		
```
