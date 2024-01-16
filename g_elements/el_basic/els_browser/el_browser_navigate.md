# Navigate

![](<../../../.gitbook/assets/image (301).png>)

Element that is used for navigation to the specified address in a web browser. The component works correctly only inside the **Open Browser** or **Attach Browser** containers.

![](<../../../.gitbook/assets/Navigate.png>)

## Properties

Symbol `*` in the property name means that it is required. Description of common properties can be found in the [Element properties](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements#svoistva-elementa) section.

- **URL\***. String. URL (address) to which navigation will be performed. 
- **Timeout\***. Int32. Maximum waiting time for process completion (ms). By default it is set to `10000`.
  
## Pure code
Below is an example of using the element in the Pure code type process:

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
app.Navigate("mail.ru");
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
app.Navigate("mail.ru")
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
app.Navigate("mail.ru");
```
{% endtab %}
{% endtabs %}
