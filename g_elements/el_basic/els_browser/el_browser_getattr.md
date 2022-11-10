# Get attribute

![](<../../../.gitbook/assets/image (177).png>)

Element that obtains the data of a control element attribute. The component works correctly only inside the Open a Browser or Connect to a Browser container.

![](<../../../.gitbook/assets/1 (56).png>)

Properties

&#x20;\- Search template: \[String] Control element search template

&#x20;\- Element: \[LTools.WebBrowser.Model.IElementInfo] Reference to a control element

&#x20;\- Attribute: \[String] Control attribute name

&#x20;\- Result: \[String] Variable for saving data of the first found attribute

&#x20;\- Result (array): \[List\<string>] Variable for saving the data of all attributes found

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search pattern
List<string> att = app.GetAttribute("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}", "title");
//Component link
LTools.WebBrowser.Model.IElementInfo el = app.FindElement("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}");
att = app.GetAttribute(el, "title");		
LTools.Workflow.PrimoApp.AddToLog(wf, att[0]);

Python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
#Search pattern
att = app.GetAttribute("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}", "title")
#Component link
el = app.FindElement("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}");
att = app.GetAttribute(el, "title");	
LTools.Workflow.PrimoApp.AddToLog(wf, att[0])

JavaScript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search pattern
var att = app.GetAttribute("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}", "title");
//Component link
var el = app.FindElement("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}");
att = app.GetAttribute(el, "title");	
_lib.LTools.Workflow.PrimoApp.AddToLog(wf, att[0]);
```
