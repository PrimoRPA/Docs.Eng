# Attach browser

Element that connects to an active browser, allowing the robot to interact with web applications, including integration with SAP through the web interface. It also serves as a container for other elements of Studio intended for the work with web applications.

![](<../../../.gitbook/assets/AttachBrowser.png>)

Note that the elements nested within the **Attach browser** container and attached to it require having a browser extension. The methods of installing extensions are described [here](https://docs.primo-rpa.ru/primo-rpa-eng/primo-studio/settings/extensions-and-plugins-install).

**Cross-platform:** works with Windows, Linux, MacOS.

## Properties
Symbol `*` in the property name means that it is required. Description of common properties can be found in the [Element properties](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements#svoistva-elementa) section.

| Property           | Type                                | Description                                                                                     |
| ------------------ | ----------------------------------- | ----------------------------------------------------------------------------------------------- |
| **Browser**        |                                     |                                                                                                 |
| Browser type       | LTools.WebBrowser.Model.BowserTypes | Defines the type of the browser used. By default it is `IE` - Internet Explorer. To select another browser, click on the dropdown list. Available values: IE, Chrome, Firefox, Opera, Edge, Yandex, SAP |
| Browser title     | String                              | Sets the title of the browser (should be specified in quotation marks ""). By default it is set to `"*"`. To add the title automatically, use **Select page** button <img src="../../../.gitbook/assets/SelectPage-button.PNG" alt="" data-size="line"> |     
| URL                | String                              | URL of the current browser page                                                                 |
| Variable           | LTools.WebBrowser.BrowserInst       | Variable that contains a reference to the earlier attached browser (if there is one)            |
| Dispose            |                                     | Determines whether the reference to the browser should be disposed of on exit                   |
| Time-out\*         | Int32                               | Maximum time of waiting for process completion (in msec). By default it is set to `10000`       |
| **SAP**            |                                     |                                                                                                 |
| Component ID       | String                              | ID of the browser component in SAP                                                              |
| Component          | LTools.SAP.Model.SAPUIItem          | Variable that contains a reference to the SAP component                                         |
| **Output**         |                                     |                                                                                                 |
| Variable           |                                     | Variable that is used to store a reference to the attached browser. Subsequently, when the **Attach browser** container is used in the process again, it can be specified for quicker connection in **Browser > Variable** property |


## Example in the Learning section

An example of the process that uses this element is available in [Learning](https://github.com/PrimoRPA/Learning/tree/master). Download StudioActivities project, open it in Studio and select `StudioActivities/Ru/Браузер/Присоединиться к браузеру.ltw` process to view it.

## Pure code
Below is an example of using the element in the Pure code type process:

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.WebBrowser.BrowserApp app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE);
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", LTools.WebBrowser.Model.BrowserTypes_Short.IE)
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.WebBrowser.BrowserApp.Init(wf, "Free email*", _lib.LTools.WebBrowser.Model.BrowserTypes_Short.IE);
```
{% endtab %}
{% endtabs %}
