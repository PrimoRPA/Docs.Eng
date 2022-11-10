# Activate window

![](<../../../.gitbook/assets/0 (106).png>)

Element that brings the process window to the fore. The component works correctly only inside the Connect to an Application container.

![](<../../../.gitbook/assets/1 (122).png>)

Properties

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, "Calc*", null, 10000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
app.Activate();

Python
app = LTools.Desktop.DesktopApp.Init(wf, "Calc*", None, 10000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
app.Activate()

JavaScript
let app = _lib.LTools.Desktop.DesktopApp.Init(wf, "Calc*", null, 10000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
app.Activate();
```
