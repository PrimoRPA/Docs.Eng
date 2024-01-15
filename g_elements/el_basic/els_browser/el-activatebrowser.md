# Activate browser

Brings the browser window to the front of the screen. This element is used when automation scenario requires working with a web interface, such as filling in forms, site navigation, data extraction, etc.

![](<../../../.gitbook/assets/ActivateBrowser.png>)

## Properties
The element has only common properties described [here](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements#svoistva-elementa). It does not have any unique properties.

## Pure code
Below is an example of using the element in the Pure code type process:

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
app.Activate();
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
app.Activate()
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
app.Activate();
```
{% endtab %}
{% endtabs %}
