# Hot-key simulation

![](<../../../.gitbook/assets/0 (87).png>)

Element that emulates the special button pressing. The component works correctly only inside the Connect to an Application container.

![](<../../../.gitbook/assets/1 (82).png>)

Properties

&#x20;\- Pause\*: \[Int32] Pause before and after pressing the buttons (ms)

&#x20;\- Special buttons\*: \[String] Pressable special buttons ({ENTER}) 'https://docs.microsoft.com/en-us/dotnet/api/system.windows.forms.sendkeys.send'

&#x20;\- Timeout\*: \[Int32] \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
app.SetFocus("{\"Name\":\"\",\"AutomationID\":\"txtbxSample\",\"ClassName\":\"TextBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
LTools.Desktop.DesktopApp.HotKeySimulate(wf, "{ENTER}");

Python
app = LTools.Desktop.DesktopApp.Init(wf, None, "Test_*", 20000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
app.SetFocus("{\"Name\":\"\",\"AutomationID\":\"txtbxSample\",\"ClassName\":\"TextBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}")
LTools.Desktop.DesktopApp.HotKeySimulate(wf, "{ENTER}")

JavaScript
var app = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
app.SetFocus("{\"Name\":\"\",\"AutomationID\":\"txtbxSample\",\"ClassName\":\"TextBox\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
_lib.LTools.Desktop.DesktopApp.HotKeySimulate(wf, "{ENTER}");
```
