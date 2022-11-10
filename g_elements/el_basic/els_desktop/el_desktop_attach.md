# Attach application

![](<../../../.gitbook/assets/0 (66).png>)

Element that connects an external application to an existing process.

![](<../../../.gitbook/assets/1 (87).png>)

Properties

&#x20; \- Automation type: Desktop application automation type

&#x20;\- Current user: \[bool] Get only current user processes

&#x20;\- Title: \[String] Header of a connected application

&#x20;\- Process name: \[String] Name of a process

&#x20;\- Variable: \[LTools.Desktop.DesktopInst] Variable containing a reference to a connected process

&#x20;\- Variable: \[LTools.Desktop.DesktopInst] Variable for saving a link to a connected process

&#x20;\- Time-out\*: \[Int32] Element finish max time (ms)

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, "Calc*", null, 10000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);

Python
app = LTools.Desktop.DesktopApp.Init(wf, "Calc*", None, 10000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)

JavaScript
let app = _lib.LTools.Desktop.DesktopApp.Init(wf, "Calc*", null, 10000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
```

