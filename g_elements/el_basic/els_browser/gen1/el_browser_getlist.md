# Get list

![](<../../../.gitbook/assets/image (197).png>)

![](<../../../.gitbook/assets/image (275).png>)



Element that gets values list from combobox or listbox.

Properties

* Search pattern: \[String] Control search pattern
* Control: \[LTools.WebBrowser.Model.IElementInfo] Control reference
* Items: \[List] All list items
* Selected: \[List] Selected list items
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Test page*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search pattern + All items
List<string> items = app.SelectGetItems("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}");
//Component link + Selected items
LTools.WebBrowser.Model.IElementInfo el = app.FindElement("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}");
items = app.SelectGetSelItems(el);

Python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Test page*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
#Search pattern + All items
items = app.SelectGetItems("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}")
#Component link + Selected items
el = app.FindElement("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}")
items = app.SelectGetSelItems(el)

JavaScript
var host = new _lib.Microsoft.ClearScript.HostFunctions();
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Test page*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search pattern + All items
var items = app.SelectGetItems("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}");
//Component link + Selected items
var el = app.FindElement("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}");
items = app.SelectGetSelItems(el);
```
