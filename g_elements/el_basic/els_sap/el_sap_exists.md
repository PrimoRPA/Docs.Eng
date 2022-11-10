# Control exists

![](<../../../.gitbook/assets/0 (27).png>)

Element that searches for a control element. The component works correctly only inside the SAP container.

![](<../../../.gitbook/assets/1 (62).png>)

Properties

&#x20;\- Element ID: \[String] ID of an element

&#x20;\- Element: \[LTools.SAP.Model.SAPUIItem] Variable to store control reference

&#x20;\- Result: \[Boolean] Variable that stores search results

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
LTools.SAP.Model.SAPUIItem item = app.ElementExists("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");

Python
app = LTools.SAP.SapApp.Init(wf)
item = app.ElementExists("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell")

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);
item = app.ElementExists("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
```
