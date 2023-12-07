# Read mail

![](<../../../../.gitbook/assets/MSExchange-ReadMail.png>)

Component that reads email from MS Exchange.

## Properties
Description of general properties can be found in the [Element properties](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements#svoistva-elementa) section.\
If the name of the property is marked with an asterisk `*`, this means that it is mandatory to specify it.


| Property             | Type                                                                   | Description                                      |
| -------------------- | ---------------------------------------------------------------------- | ------------------------------------------------ |
| Path to folder       | String                                                                 | Path to the MS Exchange folder. For example:`"Inbox"`      |
| Only unread          | Boolean                                                                | Defines whether only unread mail should be read  |
| Quantity             | Int32                                                                  | Quantity of messages to be read. By default it is set to `30` |
| Attachments          | Boolean                                                                | Defines whether email attachments should be received  |
| Query                | String                                                                 | Filter query text  |
| Shared mailbox       | String                                                                 | Specify the address of the [shared mailbox](https://learn.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes?view=exchserver-2019), if its mail should be read. For example: `"info@company.com"` |
| Variable\*           | List<[LTools.Office.Model.OMailMessage](../data-types/omailmessage.md)> | Output variable for saving the list of received emails. |

## Pure code
Example of using the element in a process of **Pure code** type:

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.Office.MSExchangeApp app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain");
List<LTools.Office.Model.OMailMessage> msg = app.ReadMail("Inbox", true, false, 10);
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain")
msg = app.ReadMail("Inbox", True, False, 10)
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.Office.MSExchangeApp.InitSvc(wf, _lib.Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain");
var msg = app.ReadMail("Inbox", true, false, 10);
```
{% endtab %}
{% endtabs %}
