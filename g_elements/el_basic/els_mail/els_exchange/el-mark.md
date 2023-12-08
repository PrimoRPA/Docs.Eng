# Mark messages

![](<../../../../.gitbook/assets/MSExchange-MarkMessages.png>)

Element that marks email messages in MS Exchange.

| Property    | Type                                                                   | Description              |
| ----------- | ---------------------------------------------------------------------- | ------------------------ |
| Mark type   | LTools.Office.Model.OMailMarkTypes                                     | Type of the message mark |
| Messages\*  | List<[LTools.Office.Model.OMailMessage](../datatypes/omailmessage.md)> | List of messages for marking |

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.Office.MSExchangeApp app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain");
List<LTools.Office.Model.OMailMessage> msg = app.ReadMail("Inbox", true, false, 10);
app.MarkMail(mag[0], LTools.Office.Model.OMailMarkTypes.IMPORTANCE_HIGH);
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain")
msg = app.ReadMail("Inbox", True, False, 10)
app.MarkMail(mag[0], LTools.Office.Model.OMailMarkTypes.IMPORTANCE_HIGH)
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.Office.MSExchangeApp.InitSvc(wf, _lib.Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain");
var msg = app.ReadMail("Inbox", true, false, 10);
app.MarkMail(mag[0], _lib.LTools.Office.Model.OMailMarkTypes.IMPORTANCE_HIGH);
```
{% endtab %}
{% endtabs %}
