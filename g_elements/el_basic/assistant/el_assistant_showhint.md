# Show hint

![](<../../../.gitbook/assets/image (231).png>)

Element that displays the hint window.

Properties:

* HTML: \[String] HTML text
* URL: \[String] Page URL
* Text: \[String] Hint text
* Font: \[String] Font name
* Font szie: \[Int32] Font size
* Font color: Font color
* Background color: Background color
* Border color: Border color
* Bold: Bold font
* Italic: Italic font
* Element color: Element highlight border color
* Control (Desktop): \[LTools.Desktop.Model.DUIControl] Desktop control reference
* Control (Browser): \[LTools.WebBrowser.Model.IElementInfo] Browser control reference
* X: \[Int32] X coord
* Y: \[Int32] Y coord
* Width: \[Int32] Tooltip width
* Height: \[Int32] Tooltip height
* Fade: Screen fade
* Localtion: Prefered location


| Property               | Type                                            | Description                     |
| ---------------------- | ----------------------------------------------- | ------------------------------- |
| Text                   | String                                          | Hint text                       |
| Font                   | String                                          | Font name                       |
| Font size              | Int32                                           | Font size                       |
| Font color             | System.Windows.Media.Color                      | Font color                      |
| Border color           | System.Windows.Media.Color                      | Border color                    |
| Bold                   | bool                                            | Bold font                       |
| Italic                 | bool                                            | Italic font                     |
| Element color          | System.Windows.Media.Color                      | Element highlight border color  |
| Do speak               | Boolean                                         | Speak text                      |
| Voice                  | String                                          | Speaker voice                   |
| Volume                 | Int32                                           | Voice volume                    |
| Speed                  | Int32                                           | Speech speed                    |
| Control (Desktop)      | LTools.Desktop.Model.DUIControl                 | Desktop control reference       |
| Control (Browser)      | LTools.WebBrowser.Model.IElementInfo            | Browser control reference       |
| X                      | Int32                                           | X coordinate                    |
| Y                      | Int32                                           | Y coordinate                    |
| Width                  | Int32                                           | Tooltip width                   |
| Hight                  | Int32                                           | Tooltip height                  |
| Fade                   | bool                                            | Screen fade                     |
| Location               | LTools.Office.Model.Assistant.PreferedLocations | Preferred tooltip location      |

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.Desktop.DesktopApp app_d = LTools.Desktop.DesktopApp.Init(wf, null, "Calc*", 10000);
var el = app_d.FindElement("{\"Name\":\"Nine\",\"AutomationID\":\"num9Button\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", 10000);

LTools.Office.AssistantApp app = new LTools.Office.AssistantApp();
app.Text = "text";
//Приложение
app.ShowHint(el, 100, 50);
//Координаты
app.ShowHint(wf, 100, 150, 100, 50);
```
{% endtab %}

{% tab title="Python" %}
```python
app_d = LTools.Desktop.DesktopApp.Init(wf, None, "Calc*", 10000)
el = app_d.FindElement("{\"Name\":\"Nine\",\"AutomationID\":\"num9Button\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", 10000)

app = LTools.Office.AssistantApp()
app.Text = "text"
#Приложение
app.ShowHint(el, 100, 50)
#Координаты
app.ShowHint(wf, 100, 150, 100, 50)
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var host = new _lib.Microsoft.ClearScript.HostFunctions();
var app_d = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "Calc*", 10000);
var el = app_d.FindElement("{\"Name\":\"Nine\",\"AutomationID\":\"num9Button\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", 10000);
var app = host.newObj(_lib.LTools.Office.AssistantApp);
app.Text = "text";
//Приложение
app.ShowHint(el, 100, 50);
//Координаты
app.ShowHint(wf, 100, 150, 100, 50);
```
{% endtab %}
{% endtabs %}

