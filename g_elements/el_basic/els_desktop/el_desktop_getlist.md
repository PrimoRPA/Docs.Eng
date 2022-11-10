# Get list

![](<../../../.gitbook/assets/image (228).png>)



Element that gets values list from combobox or listbox.

Properties

* Search pattern: \[String] Control search pattern
* Control: \[LTools.Desktop.Model.DUIControl] Control reference
* Items: \[List] All list items
* Selected: \[List] Selected list items
* Time-out\*: \[Int32] Element finish max time (ms)

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search pattern + All items
List<string> lst = app.SelectGetItems("{\"Name\":\"\",\"AutomationID\":\"lstbxListBox\",\"ClassName\":\"ListBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
//Component link + Selected items
LTools.Desktop.Model.DUIControl el = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"lstbxListBox\",\"ClassName\":\"ListBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
List<string> sel = app.SelectGetSelItems(el);

Python
app = LTools.Desktop.DesktopApp.Init(wf, None, "Test_*", 20000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
#Search pattern + All items
lst = app.SelectGetItems("{\"Name\":\"\",\"AutomationID\":\"lstbxListBox\",\"ClassName\":\"ListBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}")
#Component link + Selected items
el = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"lstbxListBox\",\"ClassName\":\"ListBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}")
sel = app.SelectGetSelItems(el)

JavaScript
var app = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search pattern + All items
var lst = app.SelectGetItems("{\"Name\":\"\",\"AutomationID\":\"lstbxListBox\",\"ClassName\":\"ListBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
//Component link + Selected items
var el = app.FindElement("{\"Name\":\"\",\"AutomationID\":\"lstbxListBox\",\"ClassName\":\"ListBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
var sel = app.SelectGetSelItems(el);
```
