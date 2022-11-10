# Kill application

![](<../../../.gitbook/assets/0 (104).png>)

Element that performs the forced termination of an external application.

![](<../../../.gitbook/assets/1 (72).png>)

Properties

&#x20; \- Current user: \[bool] Get only current user processes

&#x20;\- Automation type: Desktop application automation type

&#x20;\- Title: \[String] Header of an application connected

&#x20;\- Process name: \[String] Name of a process

&#x20;\- Time-out: \[Int32] Element finish max time (ms)

```
C#
LTools.Desktop.DesktopApp.Kill(wf, null, "Test_*", 10000, true);

Python
LTools.Desktop.DesktopApp.Kill(wf, None, "Test_*", 10000, True);

JavaScript
_lib.LTools.Desktop.DesktopApp.Kill(wf, null, "Test_*", 10000, true);
```
