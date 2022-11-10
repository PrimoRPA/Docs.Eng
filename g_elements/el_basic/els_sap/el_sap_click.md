# Mouse click

![](<../../../.gitbook/assets/0 (45).png>)

Element that mouse-clicks a selected control element. The component works correctly only inside the SAP container.

![](<../../../.gitbook/assets/1 (58).png>)

Properties

&#x20;\- Element ID: \[String] ID of ab element

&#x20;\- Element: \[LTools.SAP.Model.UIItem] Reference to a control element

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
app.Click("/app/con[0]/ses[0]/wnd[0]/tbar[0]/btn[0]");

Python
app = LTools.SAP.SapApp.Init(wf)
app.Click("/app/con[0]/ses[0]/wnd[0]/tbar[0]/btn[0]")

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);		
app.Click("/app/con[0]/ses[0]/wnd[0]/tbar[0]/btn[0]");
```
