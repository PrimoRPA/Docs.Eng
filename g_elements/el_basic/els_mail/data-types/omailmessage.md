# OMailMessage

LTools.Office.Model.OMailMessage is a mail message model. It is used in the elements that work with Outlook, Exchange, Lotus Notes mail clients.

## Model properties

| Property    | Type                                                             | Description             |
| ----------- | --------------------------------------------------------------- | -------------------- |
| ID          | String                                                          | Message identifier. Provides a way to access a specific message by its ID. The IDs can be obtained by reading messages using appropriate Studio elements. For example, the result of using [Read mail](https://docs.primo-rpa.ru/primo-rpa/g_elements/osnovnye-elementy/els_outlook/el_outlook_readmail) will be a list of messages, each of which has its own ID. |
| MailFormat  | [LTools.Office.Model.OMailMessage.MailFormats](mailformats.md)  | Message format. An example of its value is `HTML`. It can also be PLAIN (plain text) or Rich Text |
| MessageType | LTools.Office.Model.OMailMessage.MailTypes                      | Only for Outlook. Examples: `Message` or `Report` (delivery report) |
| From        | String                                                          | Email address of the sender, for example, `user@mail.ru` |
| To          | List\<String>                                                   | List of message recipients’ email addresses |
| Сс          | List\<String>                                                   | List of message copy recipients’ email addresses  |
| Всс         | List\<String>                                                   | List of message Bcc (blind carbon copy) recipients’ email addresses  |
| CreateDate  | [System.DateTime](https://learn.microsoft.com/ru-ru/dotnet/api/system.datetime?view=netframework-4.8) | Date and time when the message was created, for example, `13.07.2023 18:21:25`. Does not exist in Lotus Notes |
| ReceiveDate | System.DateTime                                                 | Date and time when the message was received. Does not exist in Lotus Notes   |
| Subject     | String                                                          | Message subject                    |
| ConversationTopic | String                                                    | Only for Outlook. A conversation includes all messages in the same thread with the same subject line. Usually, the Conversation topic is the subject line of the first email in a thread. More information about conversations can be found [here](https://support.microsoft.com/en-gb/office/view-email-messages-by-conversation-0eeec76c-f59b-4834-98e6-05cfdfa9fb07). When a message is read in Outlook, it can have both the Subject and the ConversationTopic. An example for a sent message: Subject - `"Re: Vacation"`,  ConversationTopic - `"Vacation"` |
| Body        | String                                                          | Message body text. **In Exchange, the body text will be read as HTML only**, and in Outlook it can also be read as plain text (PLAIN). Plain text does not support images, hyperlinks (they will be displayed as plain links) and other similar elements. Example for PLAIN: `"Text\n"`. When a conversation is displayed, the body will contain all emails in the conversation |
| HTMLBody    | String                                                          | Message body text in HTML format  |
| MessageProperties | LTools.Office.Model.OMailMessage.OMailProperties  | Only for Outlook. Message properties are displayed if the element [Read mail](https://docs.primo-rpa.ru/primo-rpa/g_elements/osnovnye-elementy/els_outlook/el_outlook_readmail) has **Read properties** flag. Message properties can be used, for example, to find out the display name of the sender or recipient  |
| Element     | -                                                               | Represents an email message. Data type depends on the mail client used: for Exchange it is EmailMessage, for Outlook - MailItem, for Lotus - Domino.NotesDocument. To get access to class properties, it should first be manually cast as the necessary type. More details about it are provided in the subsection below.  |
| Attachments | List<[LTools.Office.Model.OMailAttachment](omailattachment.md)> | Email attachments   |

:small_blue_diamond: **Note**. All properties that begin with the word **Send**, as well as **ReplyAll** property, contain only technical information and are not intended for users. This applies to such properties as: SendTo, SendСс, SendВсс, SendOnBehalf, ReplyAll. 


## Details 

### CreateDate
**CreateDate/ReceiveDate** model property has the following set of properties::

![](<../../../../.gitbook/assets/omail-createdate.png>)

Example of obtaining the day of the month when the message was created: `var_list_mails[0].CreateDate.Day`, where:
* var_list_mails - nominal name of the variable;
* [0] - index of the message whose property we want to obtain. 

If the result is output via the [**Add log**](https://docs.primo-rpa.ru/primo-rpa/g_elements/el_basic/els_dialogs/el_dialogs_addlog) element, make sure to cast the value as a string. Example result: `13`.

### Element

**Element** model property represents an email message. Data type depends on the email client: 
* for Exchange - it is [Microsoft.Exchange.WebServices.Data.EmailMessage](https://learn.microsoft.com/en-us/dotnet/api/microsoft.exchange.webservices.data.emailmessage?view=exchange-ews-api);
* for Outlook - it is [Microsoft.Office.Interop.Outlook.MailItem](https://learn.microsoft.com/en-us/dotnet/api/microsoft.office.interop.outlook.mailitem?view=outlook-pia);
* for Lotus - it is Domino.NotesDocument.

The list of properties will correspond to the message class. 

:bangbang: ***To obtain the value of any Element property, it has to be manually cast as the necessary class.***

For example, to obtain the sender name for an Exchange message, it should first be cast as  EmailMessage: 

`(var_list_mails[0].Element as Microsoft.Exchange.WebServices.Data.EmailMessage).Sender`. 

### MessageProperties

**MessageProperties** model property (only Outlook) has the following set of properties: 

![](<../../../../.gitbook/assets/omail-message-properties2.png>)

Their descriptions can be found in [this section](https://learn.microsoft.com/en-us/office/client-developer/outlook/mapi/mapi-properties), by selecting in the left menu the name of the canonical property. 

Example of obtaining the displayed [sender name](https://learn.microsoft.com/en-us/office/client-developer/outlook/mapi/pidtagsendername-canonical-property): `var_list_mails[0].MessageProperties.PR_SENDER_NAME`. 

It should be noted that the sender name may not be displayed - that depends on the mail server settings.
