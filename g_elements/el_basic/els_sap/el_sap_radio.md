# Radio button

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5X8lr68LfMcuUgLnql%2F-M5X9d1h1n5lD7uvIDqm%2FSAP\_%D1%80%D0%B0%D0%B4%D0%B8%D0%BE%D0%BA%D0%BD%D0%BE%D0%BF%D0%BA%D0%B0\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=7f1ad246-8f10-4125-a1ec-7e2f6d3f3725)

Element which gets reference to UI component Radio button.

![](../../../.gitbook/assets/SAP\_radio\_button.png)

Properties:

* Control ID: \[String] Control ID
* Control: \[LTools.SAP.Model.SAPUIItem] Control reference
* Radio button: \[LTools.SAP.Model.SAPUIRadioButton] Variable that stores radio button reference
* Variable: \[LTools.SAP.Model.SAPUIRadioButton] Variable to store radio button reference
* Selected: \[Boolean] Is radio button selected
* Select: Select radio button
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)

LTools.SAP.Model.SAPUIRadioButton:&#x20;

* \[SAPFEWSELib.ISapRadioButtonTarget] Element - Element reference;&#x20;
* \[String] Id - Element ID;&#x20;
* \[String] Text - Text;&#x20;
* \[bool] IsSelected - Is button selected.

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
LTools.SAP.Model.SAPUIRadioButton rad = app.RadioButton("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
rad.IsSelected = true;

Python
app = LTools.SAP.SapApp.Init(wf)
rad = app.RadioButton("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell")
rad.IsSelected = True

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);		
var rad = app.RadioButton("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
rad.IsSelected = true;
```
