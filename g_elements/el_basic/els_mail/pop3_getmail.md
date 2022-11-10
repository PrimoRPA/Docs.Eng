# Receive mail POP3

![](<../../../.gitbook/assets/image (56).png>)

Element that reads incoming messages POP3.

![](<../../../.gitbook/assets/image (297).png>)

Properties

* Server address\*: \[String] Server address
* Port\*: \[Int32] Server port
* Login\*: \[String] Login
* Password\*: \[String] Password
* SSL\*: \[Boolean] Server uses SSL connection
* Delete\*: \[Boolean] Delete messages
* Count\*: \[Int32] Messages count
* Receive attachments\*: \[Boolean] Receive attachments
* Indexes: \[System.Collections.Generic.List] Message indexes to receive
* Messages: \[System.Collections.Generic.List] Messages array
* Time-out\*: \[Int32] Message max send timeout (ms)
* Result\*: \[System.Collections.Generic.List] Received messages array

LTools.Network.Model.EMail.MailMessage - Properties:

* UID: \[String] Message ID
* Subject: \[String] Subject
* From: \[List] From
* To: \[List] To
* CC: \[List] Copy
* Date: \[DateTime?] Message date
* TextBody: \[String] Message body (text)
* HtmlBody: \[String] Message body (HTML)
* Attachments: \[List] Attachments

LTools.Network.Model.EMail.MailAttachments - Properties:

* FileName: \[String] File name
* Data: \[byte\[]] File data
