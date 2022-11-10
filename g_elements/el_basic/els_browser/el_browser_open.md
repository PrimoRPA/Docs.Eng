# Open browser

![](<../../../.gitbook/assets/image (163).png>)

Element that opens a new instance of the browser.

![](../../../.gitbook/assets/open\_browser.png)

Properties

\- Browser type: \[LTools.WebBrowser.Model.BowserTypes] Browser type

&#x20;\- Variable: \[LTools.WebBrowser.BrowserInst] Variable for saving connected browser link

```
C#
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Open(wf, LTools.WebBrowser.Model.BrowserTypes.IE);

Python
app = LTools.WebBrowser.BrowserApp.Open(wf, LTools.WebBrowser.Model.BrowserTypes.IE)

JavaScript
var app = _lib.LTools.WebBrowser.BrowserApp.Open(wf, _lib.LTools.WebBrowser.Model.BrowserTypes.IE);
```
