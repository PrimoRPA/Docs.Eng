# Combo box

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5X7WJt1Y2RYKiiHmV4%2F-M5X8diKK-LsVV2Dh71i%2FSAP\_%D0%BA%D0%BE%D0%BC%D0%B1%D0%BE-%D0%B1%D0%BE%D0%BA%D1%81\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=b865d790-74fc-4386-86d3-5329850eb886)

Element which gets reference to UI component Combo box.

![](../../../.gitbook/assets/SAP\_combo\_box.png)

Properties:

* Control ID: \[String] Control ID
* Control: \[LTools.SAP.Model.SAPUIItem] Control reference
* Combo box: \[LTools.SAP.Model.SAPUIComboBox] Variable that stores combo box reference
* Items: \[List\<LTools.SAP.Model.SAPUIComboBoxItem>] Combo box available items
* Variable: \[LTools.SAP.Model.SAPUIComboBox] Variable to store combo box reference
* Value: \[LTools.SAP.Model.SAPUIComboBoxItem] Current value
* Select (key): \[String] Select value by key
* Select (index): \[Int32] Select value by index
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)

LTools.SAP.Model.SAPUIComboBox:&#x20;

* \[SAPFEWSELib.ISapComboBoxTarget] Element - Element reference;&#x20;
* \[String] Id - Element ID;&#x20;
* \[List\<LTools.SAP.Model.SAPUIComboBoxItem>] Items - Combo box items;&#x20;
* \[SAPUIComboBoxItem] SelectedItem - Selected item;&#x20;
* SelectItem(SAPUIComboBoxItem item - item) - Select item;&#x20;
* SelectItem(int idx - item index) - Select item;&#x20;
* SelectItem(string key - item key) - Select item.

LTools.SAP.Model.SAPUIComboBoxItem:&#x20;

* \[SAPFEWSELib.ISapComboBoxEntryTarget] - Element reference;&#x20;
* \[String] Id - Item key;&#x20;
* \[String] Text - Item text;&#x20;
* \[int] Index - Item index.

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
LTools.SAP.Model.SAPUIComboBox cmb = app.ComboBox("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
cmb.SelectItem(cmb.Items[0].Id);

Python
app = LTools.SAP.SapApp.Init(wf)
cmb = app.ComboBox("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell")
cmb.SelectItem(cmb.Items[0].Id)

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);		
var cmb = app.ComboBox("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
cmb.SelectItem(cmb.Items[0].Id);
```
