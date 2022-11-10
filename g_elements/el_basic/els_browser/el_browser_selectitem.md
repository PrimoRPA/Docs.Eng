# Select item

![](<../../../.gitbook/assets/image (297).png>)

![](<../../../.gitbook/assets/image (306).png>)



Element that selects items in combobox or listbox.

Properties

* Search pattern: \[String] Control search pattern
* Control: \[LTools.WebBrowser.Model.IElementInfo] Control reference
* Item: \[String] Item to select
* Items: \[List] Items list to select
* Index: \[Int32] Item index to select
* Indexes: \[List] Items indexes to select
* Clear: Clear list before selection
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Test page*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search pattern + Item
app.SelectItem("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}", new List<string>() { "Item2" });
//Component link + Index + Clear
LTools.WebBrowser.Model.IElementInfo el = app.FindElement("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}");
app.SelectItem(el, new List<int>() { 3 }, true);

Python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Test page*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
#Search pattern + Item
app.SelectItem("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}", List[System.String](["Item2"]))
#Component link + Index + Clear
el = app.FindElement("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}")
app.SelectItem(el, List[int]([3]), True)

JavaScript
var host = new _lib.Microsoft.ClearScript.HostFunctions();
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Test page*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search pattern + Item
var items = host.newObj(_lib.System.Collections.Generic.List(_lib.System.String));
items.Add("Item2");
app.SelectItem("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}", items);
//Component link + Index + Clear
var idx = host.newObj(_lib.System.Collections.Generic.List(_lib.System.Int32));
idx.Add(3);
var el = app.FindElement("{\"Tag\":\"SELECT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"ID\",\"Value\":\"lstbxList\"}]}");
app.SelectItem(el, idx, true);
```
