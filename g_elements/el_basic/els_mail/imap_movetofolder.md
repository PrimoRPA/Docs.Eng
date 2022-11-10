# Move to folder (IMAP)

![](<../../../.gitbook/assets/image (79).png>)

Element that moves messages between folders IMAP.

![](<../../../.gitbook/assets/image (220).png>)

Properties

* Server address\*: \[String] Server address
* Port\*: \[Int32] Server port
* Login\*: \[String] Login
* Password\*: \[String] Password
* SSL\*: \[Boolean] Server uses SSL connection
* Source folder\*: \[String] Source messages folder
* Destination folder\*: \[String] Destination messages folder
* UIDs: \[System.Collections.Generic.List] Message IDs to receive
* Messages: \[System.Collections.Generic.List] Messages array
* Time-out\*: \[Int32] Message max send timeout (ms)

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
