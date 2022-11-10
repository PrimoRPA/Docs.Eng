# Attach browser

![](<../../../.gitbook/assets/0 (41).png>)

Element that connects to a valid browser.

![](<../../../.gitbook/assets/1 (36).png>)

Properties

&#x20;\- Browser type: \[LTools.WebBrowser.Model.BowserTypes] Type of a browser used

&#x20;\- Browser heading: \[String] Heading of a connected browser

&#x20;\- Variable: \[LTools.WebBrowser.BrowserInst] Variable containing a reference to a connected browser

&#x20;\- Variable: \[LTools.WebBrowser.BrowserInst] Variable for saving a link to a connected browser

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);

Python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)

JavaScript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
```
