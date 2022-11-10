# Take screenshot

![](https://gblobscdn.gitbook.com/assets%2Fprimo-rpa%2F-M-hxUXNOdBhTifh4OEN%2F-M-hxnVNbT3OZVoebQSi%2F0.png?generation=1581319142022829\&alt=media)

Element that makes desktop screenshot. In case you need to take a screenshot of any running process, the Process name should be specified. If you need a screenshot of the entire desktop, leave the Process name blank.

![](../../../.gitbook/assets/Word\_take\_screenshot.png)

Properties

&#x20;\- Title: \[String] Application title

&#x20;\- Process name: \[String] Process name

&#x20;\- Variable: \[LTools.Desktop.DesktopInst] Variable with process reference

&#x20;\- Variable: \[System.Drawing.Bitmap] Variable to store image

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Desktop
System.Drawing.Bitmap bmp = LTools.Desktop.DesktopApp.CreateScreenshot(wf);
bmp.Save(@"C:\screen1.png");
//Application by title
bmp = app.CreateScreenshot(null, "Test_*");
bmp.Save(@"C:\screen2.png");
//Current application
bmp = app.CreateScreenshot();
bmp.Save(@"C:\screen3.png");

Python
app = LTools.Desktop.DesktopApp.Init(wf, None, "Test_*", 20000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
#Desktop
bmp = LTools.Desktop.DesktopApp.CreateScreenshot(wf);
bmp.Save("C:\\screen1.png");
#Application by title
bmp = app.CreateScreenshot(None, "Test_*");
bmp.Save("C:\\screen2.png");
#Current application
bmp = app.CreateScreenshot();
bmp.Save("C:\\screen3.png");

JavaScript
var app = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "Test_*", 20000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Desktop
var bmp = _lib.LTools.Desktop.DesktopApp.CreateScreenshot(wf);
bmp.Save("C:\\screen1.png");
//Application by title
bmp = app.CreateScreenshot(null, "Test_*");
bmp.Save("C:\\screen2.png");
//Current application
bmp = app.CreateScreenshot();
bmp.Save("C:\\screen3.png");
```
