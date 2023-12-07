# Move to folder

![](<../../../../.gitbook/assets/MSExchange-MoveToFolder.png>)

Component that moves messages between folders in MS Exchange.

## Properties

Element properties are divided into groups, they are highlighted in the table with bold italic font.\
If the name of the property is marked with an asterisk `*`, this means that it is mandatory to specify it.

| Property           | Type                                                                   | Description      |
| ------------------ | ---------------------------------------------------------------------- | ---------------- |
| ***General***  | | Description of general properties can be found in the [Element properties](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements#svoistva-elementa) section. | 
| ***Exchange***  | | | 
| Destination folder\* | String                                                                 | Destination folder |
| Messages\*           | List<[LTools.Office.Model.OMailMessage](../datatypes/omailmessage.md)> | Message array |
| Shared inbox         | String  | Specify a shared inbox if messages need to be moved within it |

## Pure code
Example of using the element in a process of **Pure code** type:

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.Office.MSExchangeApp app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain");
List<LTools.Office.Model.OMailMessage> msg = app.ReadMail("Inbox", true, false, 10);
app.MoveToFolder(msg[0], "folder");
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain")
msg = app.ReadMail("Inbox", True, False, 10)
app.MoveToFolder(msg[0], "folder")
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain");
var msg = app.ReadMail("Inbox", true, false, 10);
app.MoveToFolder(msg[0], "folder");
```
{% endtab %}
{% endtabs %}
