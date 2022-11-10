# Start application



![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5fGdItHUKUM5reQNKN%2F-M5fPY15vdZHeh6x3\_p8%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9\_%D1%81%D1%82%D0%BE%D0%BB\_%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D1%82%D0%B8%D1%82%D1%8C\_%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=5e2f0484-10ff-401b-bc0a-9739cdbf0a33)

Element that starts new application process

![](<../../../.gitbook/assets/image (318).png>)

Properties

&#x20; \- Automation type: Desktop application automation type

&#x20;\- Application\*: \[String] Application name

&#x20;\- Arguments: \[String] Startup arguments

&#x20;\- Work directory: \[String] Path to process work directory&#x20;

&#x20;\- Wait start: Wait for application to start

&#x20;\- Variable: \[System.Diagnostics.Process] Variable to store new process reference

```
C#
LTools.Desktop.DesktopApp.Start(wf, "calc", null, @"c:\", LTools.Desktop.Model.DesktopTypes.UIAUTOMATION, true);

Python
LTools.Desktop.DesktopApp.Start(wf, "calc", None, "c:\\", LTools.Desktop.Model.DesktopTypes.UIAUTOMATION, True)

JavaScript
_lib.LTools.Desktop.DesktopApp.Start(wf, "calc", null, "c:\\", _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION, true);
```
