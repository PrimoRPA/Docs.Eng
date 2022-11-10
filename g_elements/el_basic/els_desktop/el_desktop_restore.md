# Restore window

![](<../../../.gitbook/assets/0 (82).png>)

Element that restores the application window. The component works correctly only inside the Connect to an Application container.

![](<../../../.gitbook/assets/1 (118).png>)

Properties

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, null, "*Notepad*", 10000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
app.Restore();

Python
app = LTools.Desktop.DesktopApp.Init(wf, None, "*Notepad*", 10000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
app.Restore()

JavaScript
var app = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "*Notepad*", 10000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
app.Restore();
```
