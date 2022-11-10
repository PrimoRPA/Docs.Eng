# Element vanish



![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5fPZgz1-4mRJtzh03l%2F-M5ff-E8r3sdtRkRHULz%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9\_%D1%81%D1%82%D0%BE%D0%BB\_%D0%B8%D1%81%D1%87%D0%B5%D0%B7%D0%BD%D0%BE%D0%B2%D0%B5%D0%BD%D0%B8%D0%B5\_%D1%8D%D0%BB\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=e14c799e-13c1-4265-88b3-bdbead1e0b8c)

Element that await for control to vanish

![](<../../../.gitbook/assets/image (327).png>)

Properties

&#x20;\- Search pattern\*: \[String] Control search pattern

&#x20;\- Time-out\*: \[Int32] Element finish max time (ms)

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
app.WaitElementVanish("{\"Name\":\"Vanish Label\",\"AutomationID\":\"\",\"ClassName\":\"TextBlock\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", 2000);

Python
app = LTools.Desktop.DesktopApp.Init(wf, None, "Test_*", 20000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
app.WaitElementVanish("{\"Name\":\"Vanish Label\",\"AutomationID\":\"\",\"ClassName\":\"TextBlock\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", 2000)

JavaScript
var app = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
app.WaitElementVanish("{\"Name\":\"Vanish Label\",\"AutomationID\":\"\",\"ClassName\":\"TextBlock\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", 2000);
```
