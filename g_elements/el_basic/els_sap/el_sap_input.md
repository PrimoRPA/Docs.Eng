# Text input

![](<../../../.gitbook/assets/0 (61).png>)

Element that enters text in a selected control element. The component works correctly only inside the SAP container.

![](<../../../.gitbook/assets/1 (52).png>)

Properties

&#x20;\- Element ID: \[String] ID of an element

&#x20;\- Element: \[LTools.SAP.Model.SAPUIItem] Reference to a control element

&#x20;\- Text\*: \[String] Text entered

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
app.TypeText("/app/con[0]/ses[0]/wnd[0]/usr/txtREPORT-LOW", "test");
LTools.SAP.Model.SAPUIItem item = app.ElementExists("/app/con[0]/ses[0]/wnd[0]/usr/txtREPORT-LOW", 10000);
app.TypeText(item, "test");

Python
app = LTools.SAP.SapApp.Init(wf);
app.TypeText("/app/con[0]/ses[0]/wnd[0]/usr/txtREPORT-LOW", "test")
item = app.ElementExists("/app/con[0]/ses[0]/wnd[0]/usr/txtREPORT-LOW", 10000)
app.TypeText(item, "test")
		
JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);		
app.TypeText("/app/con[0]/ses[0]/wnd[0]/usr/txtREPORT-LOW", "test");
var item = app.ElementExists("/app/con[0]/ses[0]/wnd[0]/usr/txtREPORT-LOW", 10000);
app.TypeText(item, "test");
```
