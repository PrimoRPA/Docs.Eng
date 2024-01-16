# Get image

![](<../../../.gitbook/assets/image (130).png>)

An element for obtaining images. The component works correctly only inside the **Open Browser** or **Attach Browser** containers.

![](<../../../.gitbook/assets/GetImage.png>)

## Properties

| Property      | Type                                 | Description                                                        |
| ------------- | ------------------------------------ | ------------------------------------------------------------------ |
| Search template | String                             | Control element search template                                    |
| Element       | LTools.WebBrowser.Model.IElementInfo | Reference to the control element                                   |
| Attribute     | String                               | Control attribute name containing the URL of the image             |
| Image\*       | byte\[]                              | Variable for saving the data of the obtained image                 |
| URL           | String                               | Image URL                                                          |
| Timeout\*     | Int32                                | Maximum waiting time for process completion (ms)                   |


{% tabs %}
{% tab title="C#" %}
```csharp
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//By attribute
byte[] img = app.GetImage("{\"Tag\":\"IMG\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"lazyImg\"}]}", "src");	
//By URL
img = LTools.WebBrowser.BrowserApp.GetImage(wf, "https://i0.mail.com/mcom/574/10358574%2Cpd=2%2Cf=teaser-card-s/.jpg");
System.IO.File.WriteAllBytes(@"C:\image.png", img);
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
#By attribute
img = app.GetImage("{\"Tag\":\"IMG\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"lazyImg\"}]}", "src")
#By URL
img = LTools.WebBrowser.BrowserApp.GetImage(wf, "https://i0.mail.com/mcom/574/10358574%2Cpd=2%2Cf=teaser-card-s/.jpg")
System.IO.File.WriteAllBytes("C:\\image.png", img)
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//By attribute
var img = app.GetImage("{\"Tag\":\"IMG\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"lazyImg\"}]}", "src");	
//By URL
img = _lib.LTools.WebBrowser.BrowserApp.GetImage(wf, "https://i0.mail.com/mcom/574/10358574%2Cpd=2%2Cf=teaser-card-s/.jpg");
_lib.System.IO.File.WriteAllBytes("C:\\image.png", img);
```
{% endtab %}
{% endtabs %}
