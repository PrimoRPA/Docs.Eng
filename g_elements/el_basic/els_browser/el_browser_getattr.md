# Get attribute

![](<../../../.gitbook/assets/image (177).png>)

Element that obtains the data of a control element attribute. The component works correctly only inside the **Open a Browser** or **Attach Browser** container.

For the element to work properly, do the following:
1. Place the component inside a container - [**Open browser**](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/els_browser/el_browser_open) or [**Attach browser**](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/els_browser/el_browser_attach).
2. [Install the extension](https://docs.primo-rpa.ru/primo-rpa-eng/primo-studio/settings/extensions-and-plugins-install) for the browser you want to connect to.

![](<../../../.gitbook/assets/GetAttribute.png>)

## Properties

Symbol `*` in the property name means that it is required. Description of common properties can be found in the [Element properties](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements#svoistva-elementa) section.

**«Process» group**:

- **Attribute**: String. Control element attribute name, for example: `"title"`.
- **Timeout\***: Int32. Maximum waiting time for process completion (ms). By default it is set to `10000`. 
- **Search template**: String. [Search template](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/searchpatterns) of the control element (the same as selector). To create a template quickly, use **Select component** tool ![](<../../../.gitbook/assets/image (553).png>)
- **Element**: LTools.WebBrowser.Model.IElementInfo. Variable with a reference to the control element. It can filled if the required control element was found earlier using **Browser exists** component.

**«Output» group**:

- **Result**: String. Variable for saving data of the first found attribute.
- **Result (array)**: List\<string>. Variable for saving the data of all attributes found.

## Pure code
Below is an example of using the element in the Pure code type process:

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search template
List<string> att = app.GetAttribute("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}", "title");
//Element
LTools.WebBrowser.Model.IElementInfo el = app.FindElement("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}");
att = app.GetAttribute(el, "title");		
LTools.Workflow.PrimoApp.AddToLog(wf, att[0]);
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
#Search template
att = app.GetAttribute("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}", "title")
#Element
el = app.FindElement("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}");
att = app.GetAttribute(el, "title");	
LTools.Workflow.PrimoApp.AddToLog(wf, att[0])
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
//Search template
var att = app.GetAttribute("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}", "title");
//Element
var el = app.FindElement("{\"Tag\":\"INPUT\",\"SearchFrames\":false,\"Attributes\":[{\"Key\":\"CLASS\",\"Value\":\"textbox js-hide-label\"},{\"Key\":\"ID\",\"Value\":\"header-search-input\"}]}");
att = app.GetAttribute(el, "title");	
_lib.LTools.Workflow.PrimoApp.AddToLog(wf, att[0]);
```
{% endtab %}
{% endtabs %}



