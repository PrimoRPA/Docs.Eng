# Send mail

![](<../../../../.gitbook/assets/MSExchange-SendMail.png>)

Component for sending mail messages using MS Exchange. This components works correctly only within the [**MS Exchange server**](https://docs.primo-rpa.ru/primo-rpa-eng/g_elements/el_basic/els_mail/els_exchange/el_connect) container.

General properties of the element are described [here](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements). Specific ones are shown in the table below. 

Please note that all properties except **To** are not mandatory. If only the recipient is specified, a blank email will be sent.

| Property      | Type                                                                       | Description                       
| ------------- | -------------------------------------------------------------------------- | ------------------------------ 
| To            | String                                                                     | Mail recipient. Mandatory field   
| Variable    | [LTools.Office.Model.OMailMessage](../data-types/omailmessage.md)            | Message data 
| Subject       | String                                                                     | Message subject                 
| Message body  | String                                                                     | Body of the message   
| Attachments   | List\<String>                                                              | Path to email attachment files             
| Cc            | String                                                                     | Send a copy             
| Bcc           | String                                                                     | Send a Bcc (blind carbon copy)     
| From          | String                                                                     | Specified if the sender needs to be changed. Specify the email address alias, for example: "iv_ivan@mail.ru". Note that the email address should be on the list of addresses of the mail server (for more details, see [this](https://learn.microsoft.com/en-us/microsoft-365/admin/email/add-another-email-alias-for-a-user?view=o365-worldwide) and [this](https://learn.microsoft.com/en-us/microsoft-365/admin/add-users/give-mailbox-permissions-to-another-user?view=o365-worldwide)). If no value is specified, the default sender will be the owner of the account, with which connection to MS Exchange server is established.     
| Format        | [Tools.Office.Model.OMailMessage.MailFormats](../data-types/mailformats.md) | Message format              
| Copy to folder | Boolean                                                                 | Make a copy of the message after sending 
| Copy folder   | String                                                                   | Folder name for saving message copy  
| **Re: group**    |            |        
| Reply         | [LTools.Office.Model.OMailMessage](../data-types/omailmessage.md)           | Reply to the message              
| Reply all     | Boolean                                                                    | If this flag is set, reply will be sent to all recipients        


{% tabs %}
{% tab title="C#" %}
```csharp
LTools.Office.MSExchangeApp app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain");
LTools.Office.Model.OMailMessage msg = new LTools.Office.Model.OMailMessage() { Subject = "subject", Body = "body" };
app.SendMessage(msg);
app.SendMessage("body", "sendTo", "subject", new List<string>() { "file1" }, LTools.Office.Model.OMailMessage.MailFormats.HTML);
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain")
msg = LTools.Office.Model.OMailMessage() 
msg.Subject = "subject"
msg.Body = "body"
app.SendMessage(msg)
att = List[String]()
att.Add("file1")
app.SendMessage("body", "sendTo", "subject", att, LTools.Office.Model.OMailMessage.MailFormats.HTML)
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var host = new _lib.Microsoft.ClearScript.HostFunctions();
var app = _lib.LTools.Office.MSExchangeApp.InitSvc(wf, _lib.Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain");
var msg = host.newObj(_lib.LTools.Office.Model.OMailMessage); 
msg.Subject = "subject";
msg.Body = "body";
var att = host.newObj(_lib.System.Collections.Generic.List(_lib.System.String));
att.Add("file1");
app.SendMessage(msg);
app.SendMessage("body", "sendTo", "subject", att, _lib.LTools.Office.Model.OMailMessage.MailFormats.HTML);
```
{% endtab %}
{% endtabs %}
