# Save mail

![](<../../../../.gitbook/assets/MSExchange-SaveMail.png>)

Component that saves to disk email messages from MS Exchange. This components works correctly only within the [**MS Exchange server**](https://docs.primo-rpa.ru/primo-rpa-eng/g\_elements/el\_basic/els\_mail/els\_exchange/el\_connect) container.


> _Description of general properties can be found in the [Working with elements](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements) section._

If the name of the property is marked with an asterisk `*`, this means that it is mandatory to specify it.


| Property    | Type                                                                       | Description                            |
| ----------- | -------------------------------------------------------------------------- | -------------------------------------- |
| Path\*      | String                                                                     | Path for saving the file in \*.eml format |
| Message\*   | [LTools.Office.Model.OMailMessage](../els\_mail/data-types/omailmessage.md) | Message to be saved, a variable       |

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.Office.MSExchangeApp app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "URL", "login", "pass", "domain");
app.SaveMessage(msg, @"C:\file.eml");
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "URL", "login", "pass", "domain")
app.SaveMessage(msg, "C:\file.eml")
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.Office.MSExchangeApp.InitSvc(wf, _lib.Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "URL", "login", "pass", "domain");
app.SaveMessage(msg, "C:\\file.eml");
```
{% endtab %}
{% endtabs %}
