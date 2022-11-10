# Check box

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5\_tH7B2bLgime51IUT%2F-M5\_vJVOhyEgF3E7HsKW%2FSAP\_%D1%87%D0%B5%D0%BA%D0%B1%D0%BE%D0%BA%D1%81\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=1a9da575-d730-4086-a289-c7b65f4f3e19)

Element which gets reference to UI component Check box.

![](../../../.gitbook/assets/SAP\_check\_box.png)

Properties:

* Control ID\*: \[String] Control ID
* Control: \[LTools.SAP.Model.SAPUIItem] Control reference
* Check box: \[LTools.SAP.Model.SAPUICheckBox] Variable that stores check box reference
* Variable: \[LTools.SAP.Model.SAPUICheckBox] Variable to store check box reference
* State: \[Boolean] Check box state
* Change state: Determines that state must be changed
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)

LTools.SAP.Model.SAPUICheckBox:&#x20;

* \[SAPFEWSELib.ISapCheckBoxTarget] Element - Element reference;&#x20;
* \[String] Id - Element ID;&#x20;
* \[int] Color - Color;&#x20;
* \[bool] IsChecked - Is checked property.

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
LTools.SAP.Model.SAPUICheckBox ch = app.CheckBox("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
ch.IsChecked = true;

Python
app = LTools.SAP.SapApp.Init(wf)
ch = app.CheckBox("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell")
ch.IsChecked = True

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);
var ch = app.CheckBox("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
ch.IsChecked = true;
```
