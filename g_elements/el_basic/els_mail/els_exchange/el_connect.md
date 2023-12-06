# MS Exchange server


![](<../../../../.gitbook/assets/image (366).png>)

This element establishes connection to Microsoft Exchange server and enables a robot to interact with it to perform operations with email. 

It is a container for other elements that are part of the `MS Exchange` group (see illustration below), which are used for sending/receiving email, attaching files to messages, extracting attachments and other email operations.

![](<../../../../.gitbook/assets1/items-from-groups-ms-exchange.png>)

## Properties

Description of general properties can be found in the [Element properties](https://docs.primo-rpa.ru/primo-rpa/primo-studio/process/elements#svoistva-elementa) section.\
If the name of the property is marked with an asterisk `*`, this means that it is mandatory to specify it.

| Property           | Type                                                   | Description                                                                     |
| ------------------ | ---------------------------------------------------- | ---------------------------------------------------------------------------- |
| ***Exchange*** |  |  |
| Version             | Microsoft.Exchange.WebServices. Data.ExchangeVersion | Version of MS Exchange server. By default, `Exchange2013_SP1` version is set. To select another version, click on the dropdown list. |
| Server URL         | String                                               | URL of MS Exchange server. Example: `"https://<server>/EWS/Exchange.asmx"`      |
| E-mail             | String                                               | Specify user email to use autodiscovery of the URL for Exchange web services (EWS) endpoint. Example: `"user1@example.com"`  |
| Domain              | String                                               | Domain name                                                                   |
| Login              | String                                               | User login                                                           |
| Password             | String                                               | Password of the Exchange account                                               |
| Secure password |[SecureString](https://learn.microsoft.com/ru-ru/dotnet/api/system.security.securestring?view=netcore-2.0) | Field for the encrypted password. For security purposes the password in SecureString format is not stored openly. It can be obtained, for example, from **Credential Manager** application |
| Russian time zone | Boolean                                         | This setting is meant for time corrections. For example, if the time zone is determined incorrectly in the Russian localized version. Disabled by default.  |

:small_orange_diamond: **Important!** For successful extraction of email attachments it is necessary to enable the **Russian time zone** property.

## Learning
There is a sample RPA project available to practice using the **MS Exchange server** element. It can be accessed by [downloading a Learning archive](https://github.com/PrimoRPA/Learning/archive/refs/heads/master.zip).

1. Download the archive with training materials using the link specified above.
2. Unpack the archive and open `StudioActivities` project in Studio.
3. Find `StudioActivities/Ru/Почта/MS Exchange/Основы.ltw` process in the project. 


## Pure code
Example of using the element in a process of **Pure code** type:

{% tabs %}
{% tab title="C#" %}
```csharp
LTools.Office.MSExchangeApp app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain");
LTools.Office.MSExchangeApp app2 = LTools.Office.MSExchangeApp.InitAd(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "autodiscovery url", "login", "pass", "domain");
```
{% endtab %}

{% tab title="Python" %}
```python
app = LTools.Office.MSExchangeApp.InitSvc(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain")
app2 = LTools.Office.MSExchangeApp.InitAd(wf, Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "autodiscovery url", "login", "pass", "domain")
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
var app = _lib.LTools.Office.MSExchangeApp.InitSvc(wf, _lib.Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "server url", "login", "pass", "domain");
var app = _lib.LTools.Office.MSExchangeApp.InitAd(wf, _lib.Microsoft.Exchange.WebServices.Data.ExchangeVersion.Exchange2013_SP1, "autodiscovery url", "login", "pass", "domain");
```
{% endtab %}
{% endtabs %}
