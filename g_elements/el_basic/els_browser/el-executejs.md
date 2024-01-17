# Execute JS

This element is intended for running JavaScript code in the browser. It can be used to change page contents, to interact with data,  and to emulate user actions. 

It is recommended to use this element inside a container: [**Open Browser**](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/els_browser/el_browser_open) or 
[**Attach Browser**](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/els_browser/el_browser_attach). Browser type should be specified in the container. 

![](<../../../.gitbook/assets/ExecuteJS-container.png>)

## Properties
Symbol `*` in the property name means that it is required. Description of common properties can be found in the [Element properties](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements#svoistva-elementa) section.

**«Process» group:**

1. **Script\***. String. Enter here the script that needs to be executed. Note that quotation marks inside the string should be escaped. If the script declares a function, the following template should be used: `"function test(a, v, el) { alert(v); return null; }"`. Where v - is an argument.
2. **Time-out\***. Int32. Maximum waiting time for process completion (ms). By default it is set to `10000`.

**«Function» group:**

1. **Function**. Boolean. Mark this checkbox if the script contains a function. By default the checkbox is not marked.
2. **Argument**. String. Works only with the **Function** property enabled. Use this field to specify the argument of the function. An argument can be a specific value (for example, `"hello"`), or a string variable. Only one argument can be used.
3. **Search pattern**. This property is used to select the web page control where the script will be run. Use **Magic wand** tool to create a search template quickly. More information about search patterns can be found [here](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/searchpatterns). Requires a [browser extension](https://docs.primo-rpa.ru/primo-rpa-eng/primo-studio/settings/extensions-and-plugins-install).

    ![](<../../../.gitbook/assets/ExecuteJS-magicwand.png>) 

4. **Control**. LTools.WebBrowser.Model.IElementInfo. In this property you can specify a variable that contains a reference to a web control.
  
   How to get it:
   * In the script first use the [**Element exists**](https://docs.primo-rpa.ru/primo-rpa/g_elements/el_basic/els_uiinteraction/el_exists) component. In the **Control** output property of this component, specify a variable of the [UIControl](https://docs.primo-rpa.ru/primo-rpa/g_elements/el_basic/els_uiinteraction/datatypes/uicontrol) type - it will store a reference to the control.
   * In the **Control** property of the **Execute JS** component, open the code editor and specify `<variable name>.BrowserElement`.
  
     ![](<../../../.gitbook/assets/ExecuteJS-property.png>)                                                                  

**«Output» group:**
1. **Result**. String. Variable for storing the script execution result.     

## Pure code
Below is an example of using the element in the Pure code type process:

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Test page*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
app.Eval("script", 10000);
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Test page*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
app.Eval("script", 10000)
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Test page*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
app.Eval("script", 10000);
```
{% endtab %}
{% endtabs %} 
