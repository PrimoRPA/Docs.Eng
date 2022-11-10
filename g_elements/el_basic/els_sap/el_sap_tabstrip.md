# Tab strip

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5X3utkzcv5tvaBuG83%2F-M5X5ITI6EK4FSbWa0Gt%2FSAP\_%D0%B7%D0%B0%D0%BA%D0%BB%D0%B0%D0%B4%D0%BA%D0%B8\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=328e2758-4eb4-4852-9318-3cf78b45c95b)

Element which gets reference to UI component Tab strip.

![](../../../.gitbook/assets/SAP\_tab\_strip.png)

Properties:

* Control ID: \[String] Control ID
* Control: \[LTools.SAP.Model.SAPUIItem] Control reference
* Tab strip: \[LTools.SAP.Model.SAPUITabStrip] Variable that stores tab strip reference
* Variable: \[LTools.SAP.Model.SAPUITabStrip] Variable to store tabs reference
* Items: \[List\<LTools.SAP.Model.SAPUITab>] Tab strip items
* Select (key): \[String] Select tab by key
* Select (index): \[Int32] Select tab by index
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)

LTools.SAP.Model.SAPUITabStrip:&#x20;

* \[SAPFEWSELib.ISapTabbedPane] Element - Element reference;&#x20;
* \[String] Id - Element ID;&#x20;
* \[List\<LTools.SAP.Model.SAPUITab>] Tabs - Tabs;&#x20;
* SelectTab(SAPUITab tab - tab) - Select tab;&#x20;
* SelectTab(int idx - tab index) - Select tab;&#x20;
* SelectTab(string key - tab key) - Select tab.

LTools.SAP.Model.SAPUITab:&#x20;

* \[SAPFEWSELib.ISapTabTarget] - Element reference;&#x20;
* \[String] Id - Tab key;&#x20;
* \[String] Text - Tab text.

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
LTools.SAP.Model.SAPUITabStrip tabs = app.TabStrip("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
tabs.SelectTab(tabs.Tabs[0].Id);

Python
app = LTools.SAP.SapApp.Init(wf);
tabs = app.TabStrip("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell")
tabs.SelectTab(tabs.Tabs[0].Id)

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);		
var tabs = app.TabStrip("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
tabs.SelectTab(tabs.Tabs[0].Id);
```
