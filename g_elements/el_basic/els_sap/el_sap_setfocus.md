# Set focus

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5\_s\_aHg5cY66bHEFsd%2F-M5\_tEHb0w\_DHrRi-vBV%2FSAP\_%D1%84%D0%BE%D0%BA%D1%83%D1%81%20%D0%B2%D0%BE%D0%BE%D0%B4%D0%B0\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=fc178bb3-e268-4b0e-a266-5ed0d8237bbe)

Component that sets the input focus on a selected control element.

![](../../../.gitbook/assets/SAP\_set\_focus.png)

Properties

&#x20;\- Control ID: \[String] Control ID

&#x20;\- Control: \[LTools.SAP.Model.SAPUIItem] Control reference

&#x20;\- Time-out\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
app.SetFocus("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");

Python
app = LTools.SAP.SapApp.Init(wf)
app.SetFocus("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell")

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);
app.SetFocus("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
```
