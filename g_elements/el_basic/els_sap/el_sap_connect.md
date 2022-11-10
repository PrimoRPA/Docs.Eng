# Attach SAP

![](<../../../.gitbook/assets/0 (2).png>)

Element that connects to the opened SAP Front End application.

![](<../../../.gitbook/assets/1 (59).png>)

Properties

&#x20;\- Variable: \[LTools.SAP.SAPInst] Variable for saving a reference to a connected process

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);

Python
app = LTools.SAP.SapApp.Init(wf)

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);
```
