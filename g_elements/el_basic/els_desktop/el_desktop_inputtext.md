# Text input

![](<../../../.gitbook/assets/0 (74).png>)

Element entering text in a selected control element. The component works correctly only inside the Connect to an Application container.

![](<../../../.gitbook/assets/1 (101).png>)

Properties

&#x20;\- Search template: \[String] Control element search template

&#x20;\- Element: \[LTools.Desktop.Model.DUIControl] Reference to a control element

&#x20;\- Text\*: \[String] Text entered

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)

```
C#
LTools.Desktop.DesktopApp app = LTools.Desktop.DesktopApp.Init(wf, null, "Calc*", 10000, true, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search pattern
app.TextInput("{\"AutomationID\":\"CalculatorResults\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", "11");
//Component link
LTools.Desktop.Model.DUIControl el = app.FindElement("{\"AutomationID\":\"CalculatorResults\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
app.TextInput(el, "11");

Python
app = LTools.Desktop.DesktopApp.Init(wf, None, "Calc*", 10000, True, LTools.Desktop.Model.DesktopTypes.UIAUTOMATION)
#Search pattern
app.TextInput("{\"AutomationID\":\"CalculatorResults\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", "11")
#Component link
el = app.FindElement("{\"AutomationID\":\"CalculatorResults\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}")
app.TextInput(el, "11")

JavaScript
let app = _lib.LTools.Desktop.DesktopApp.Init(wf, null, "Calc*", 10000, true, _lib.LTools.Desktop.Model.DesktopTypes.UIAUTOMATION);
//Search pattern
app.TextInput("{\"AutomationID\":\"CalculatorResults\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}", "11");
//Component link
let el = app.FindElement("{\"AutomationID\":\"CalculatorResults\",\"AUIProperties\":[],\"TextSearchMode\":0,\"IsRoot\":false,\"IsQuickSearch\":false}");
app.TextInput(el, "11");
```
