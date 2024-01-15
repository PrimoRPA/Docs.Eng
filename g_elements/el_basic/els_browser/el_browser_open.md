# Open browser

![](../../../.gitbook/assets/open\_browser.png)

This element performs two main functions:
1. Opens a new instance of a browser or a new tab in the already open browser. **Note**: for Internet Explorer, only a new instance will be opened. 
2. Serves as a container for other elements that work with web pages. For example, such elements as [**Element exists**](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/els_uiinteraction/el_exists), [**Mouse click**](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/els_uiinteraction/el_click), [**Refresh**](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/els_browser/el_refresh), etc.


   ![](<../../../.gitbook/assets/OpenBrowser-as-container-cropped.png>)

   Elements nested within and attached to the **Open browser** container require a browser extension, although the container itself works independently of it. Methods for installing extensions are described [here](https://docs.primo-rpa.ru/primo-rpa-eng/primo-studio/settings/plugin-install).

**Cross-platform:** works in Windows, Linux, MacOS.
   
## Properties
Symbol `*` in the property name means it is required. Description of common properties can be found in the following section: [Working with elements](https://docs.primo-rpa.ru/primo-rpa-eng/primo-studio/elements).

**«Browser» group**:

1. **URL**. String. Page URL, for example, `"https://primo-rpa.ru/"`.
2. **Browser type**. The type of the browser being used. By default it is set to `IE` - Internet Explorer. To select another value, click to access the dropdown list:

   ![](<../../../.gitbook/assets/BrowserTypes.PNG>)

   Values that start with the words `Web Driver` are intended for the cases when it is necessary to use Selenium WebDriver. The web driver is built into Studio by default but to work successfully the versions of the driver and the browser must match. If they are not compatible, the web drive needs to be [updated](https://docs.primo-rpa.ru/primo-rpa-eng/primo-studio/settings/update-web-driver).
   
4. **Dispose**. Boolean. Determines whether browser reference will be released on exit. By default this checkbox is disabled - the reference is not released. 
5. **Hide**. Boolean. Only for use with the WebDriver, except Edge. Determines whether the browser should be started as invisible to the user - it will work in the background. By default this checkbox is disabled. 
 
**«Output» group**:

**Variable**. LTools.WebBrowser.BrowserInst. Here you can specify the variable for saving a link to the connected browser. 

### Browser does not open

If the desired result wasn’t achieved by using this element, check the following:

- The system has the browser installed that matches the one selected in the **Browser type** property;
- User access rights for using the browser;
- Error description in the console.

## Pure code

Below are examples of using the element in **Pure code** type processes:

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Open(wf, LTools.WebBrowser.Model.BrowserTypes.IE);
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.WebBrowser.BrowserApp.Open(wf, LTools.WebBrowser.Model.BrowserTypes.IE)
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.WebBrowser.BrowserApp.Open(wf, _lib.LTools.WebBrowser.Model.BrowserTypes.IE);
```
{% endtab %}
{% endtabs %}
