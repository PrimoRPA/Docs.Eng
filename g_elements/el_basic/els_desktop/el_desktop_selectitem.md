# Select item

![](<../../../.gitbook/assets/image (139).png>)



Element that selects items in combobox or listbox.

Properties

* Search pattern: \[String] Control search pattern
* Control: \[LTools.Desktop.Model.DUIControl] Control reference
* Item: \[String] Item to select
* Items: \[List] Items list to select
* Index: \[Int32] Item index to select
* Indexes: \[List] Items indexes to select
* Clear: Clear list before selection
* Time-out\*: \[Int32] Element finish max time (ms)

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 10000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search pattern + Value
app.SelectItem("{\"Name\":\"\",\"AutomationID\":\"cmbbxCombo\",\"ClassName\":\"ComboBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", new List<string>() { "Item1" });
//Comnonent link + Index + Clear
LTools.Desktop.Model.DUIControl el = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"cmbbxCombo\",\"ClassName\":\"ComboBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
app.SelectItem(el, new List<int>() { 2 }, true);

Python
app = LTools.Desktop.DesktopApp.Init(wf, None, "Test_*", 10000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
#Search pattern + Value	
app.SelectItem("{\"Name\":\"\",\"AutomationID\":\"cmbbxCombo\",\"ClassName\":\"ComboBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", List[String](["Item1"]));
#Comnonent link + Index + Clear
el = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"cmbbxCombo\",\"ClassName\":\"ComboBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
app.SelectItem(el, List[int]([2]), True);

JavaScript
var host = new _lib.Microsoft.ClearScript.HostFunctions();
var app = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 10000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search pattern + Value
var items = host.newObj(_lib.System.Collections.Generic.List(_lib.System.String));
items.Add("Item1");
app.SelectItem("{\"Name\":\"\",\"AutomationID\":\"cmbbxCombo\",\"ClassName\":\"ComboBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", items);
//Comnonent link + Index + Clear
var idx = host.newObj(_lib.System.Collections.Generic.List(_lib.System.Int32));
idx.Add(2);
var el = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"cmbbxCombo\",\"ClassName\":\"ComboBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
app.SelectItem(el, idx, true);
```
