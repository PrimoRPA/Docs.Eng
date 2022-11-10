# Open SAP

![](<../../../.gitbook/assets/0 (39).png>)

Element that connects to SAP Front End.

![](<../../../.gitbook/assets/1 (25).png>)

**Notice! This element works correctly in robot x86 only!**

Properties

&#x20;\- Connection\*: \[String] Name of connection in SAP Logon

&#x20;\- Client\*: \[String] Client number (000-999)

&#x20;\- Login\*: \[String] User login

&#x20;\- Password\*: \[String] User password

&#x20;\- Connection language\*: \[String] Connection language

&#x20;\- Variable: \[LTools.SAP.SAPInst] Variable containing a reference to a connected process

&#x20;\- Variable: \[LTools.SAP.SAPInst] Variable for saving a reference to a connected process

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf, "test2", "001", "DEVELOPER", "Appl1ance", "en");

Python
app = LTools.SAP.SapApp.Init(wf, "test2", "001", "DEVELOPER", "Appl1ance", "en")

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf, "test2", "001", "DEVELOPER", "Appl1ance", "en");
```
