# Calendar

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5X5iD\_INJLmVYexWcL%2F-M5X7P\_Fh3W-ziyWQ3jt%2FSAP\_%D0%BA%D0%B0%D0%BB%D0%B5%D0%BD%D0%B4%D0%B0%D1%80%D1%8C\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=dbc655f1-36c9-4bdd-849c-b5c78c3680c0)

Element which gets reference to UI component Calendar.

![](../../../.gitbook/assets/SAP\_calendar.png)

Properties:

* Control ID\*: \[String] Control ID
* Control: \[LTools.SAP.Model.SAPUIItem] Control reference
* Calendar: \[LTools.SAP.Model.SAPUICalendar] Variable that stores calendar reference
* Variable: \[LTools.SAP.Model.SAPUICalendar] Variable to store calendar reference
* Date: \[DateTime?] Focused date
* Range - start: \[DateTime?] Date range - start
* Range - end: \[DateTime?] Date range - end
* Date: \[DateTime?] Focus date
* Range - start: \[DateTime?] Date range - start
* Range - end: \[DateTime?] Date range - end
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)

LTools.SAP.Model.SAPUICalendar:&#x20;

* \[SAPFEWSELib.ISapCalendar] Element - Element reference;&#x20;
* \[String] Id - Element ID;&#x20;
* \[DateTime?] SelectionStart - Date range start;&#x20;
* \[DateTime?] SelectionEnd - Date range end;&#x20;
* \[DateTime?] FocusedDate - Focused date;&#x20;
* SelectRange(DateTime from - start, DateTime to - end) - Choose date range.

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
LTools.SAP.Model.SAPUICalendar cal = app.Calendar("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
cal.SelectRange(new DateTime(2020, 2, 24), DateTime.Now);

Python
app = LTools.SAP.SapApp.Init(wf)
cal = app.Calendar("/app/con[0]/ses[0]/wnd[0]/usr/cntlCALE_CONTROL/shellcont/shell/shellcont[0]/shell")
cal.SelectRange(DateTime(2020, 2, 24), DateTime.Now)

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);		
var cal = app.Calendar("/app/con[0]/ses[0]/wnd[0]/usr/cntlCALE_CONTROL/shellcont/shell/shellcont[0]/shell");
cal.SelectRange(new _lib.System.DateTime(2020, 2, 24), _lib.System.DateTime.Now);
```
