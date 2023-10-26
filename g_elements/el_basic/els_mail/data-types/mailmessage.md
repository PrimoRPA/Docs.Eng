# MailMessage

LTools.Network.Model.EMail.MailMessage

| Property    | Type                                       | Description             |
| ----------- | ------------------------------------------ | ----------------------- |
| UID         | String                                     | Message identifier      |
| Subject     | String                                     | Message subject         |
| From        | List\<String>                              | Sender                  |
| To          | List\<String>                              | Recipient               |
| CC          | List\<String>                              | Copy                    |
| Date        | DateTime?                                  | Message date            |
| TextBody    | String                                     | Message body (text)     |
| HtmlBody    | String                                     | Message body (HTML)     |
| Attachments | List<[MailAttachment](mailattachments.md)> | Attachments             |
