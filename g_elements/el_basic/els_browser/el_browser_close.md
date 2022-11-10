# Close browser

![](<../../../.gitbook/assets/image (161).png>)

Element that stops a browser. The component works correctly only inside the Open a Browser or Connect to a Browser container.

```
C#
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
app.Close();

Python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
app.Close()

JavaScript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
app.Close();
```
