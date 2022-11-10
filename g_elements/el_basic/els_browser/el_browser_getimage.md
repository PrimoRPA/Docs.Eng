# Get image

![](<../../../.gitbook/assets/image (130).png>)

Element obtaining images. The component works correctly only inside the Open a Browser or Connect to a Browser container.

![](<../../../.gitbook/assets/1 (18).png>)

Properties

&#x20;\- Search template: \[String] Control element search template

&#x20;\- Element: \[LTools.WebBrowser.Model.IElementInfo] Reference to a control element

&#x20;\- Attribute: \[String] Control attribute name containing the URL of an image

&#x20;\- Image\*: \[byte\[]] Variable for saving the data of the received image

&#x20;\- URL: \[String] Image URL

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//By attribute
byte[] img = app.GetImage("{\"Tag\":\"IMG\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"lazyImg\"}]}", "src");	
//By URL
img = LTools.WebBrowser.BrowserApp.GetImage(wf, "https://i0.mail.com/mcom/574/10358574%2Cpd=2%2Cf=teaser-card-s/.jpg");
System.IO.File.WriteAllBytes(@"C:\image.png", img);

Python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
#By attribute
img = app.GetImage("{\"Tag\":\"IMG\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"lazyImg\"}]}", "src")
#By URL
img = LTools.WebBrowser.BrowserApp.GetImage(wf, "https://i0.mail.com/mcom/574/10358574%2Cpd=2%2Cf=teaser-card-s/.jpg")
System.IO.File.WriteAllBytes("C:\\image.png", img)

JavaScript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//By attribute
var img = app.GetImage("{\"Tag\":\"IMG\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"lazyImg\"}]}", "src");	
//By URL
img = _lib.LTools.WebBrowser.BrowserApp.GetImage(wf, "https://i0.mail.com/mcom/574/10358574%2Cpd=2%2Cf=teaser-card-s/.jpg");
_lib.System.IO.File.WriteAllBytes("C:\\image.png", img);
```
