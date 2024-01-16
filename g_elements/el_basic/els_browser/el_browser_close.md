# Close browser

![](<../../../.gitbook/assets/image (161).png>)

Element that stops a browser. It can be used when it is necessary to stop the work with the browser after completing all necessary actions. For example, once all necessary data from a webpage has been collected, closing the browser will help release resources and finish the current process of the robot. 

![](<../../../.gitbook/assets/CloseBrowser.png>)

The component works correctly only inside the [**Open a Browser**](g_elements/el_basic/els_browser/el_browser_open.md) or [**Connect to a Browser**](g_elements/el_basic/els_browser/el_browser_attach.md) container.

## Properties

The element has only common properties described [here](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements#svoistva-elementa). It does not have any unique properties.


## Pure code
Below is an example of using the element in the Pure code type process:

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
app.Close();
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
app.Close()
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
app.Close();
```
{% endtab %}
{% endtabs %}


