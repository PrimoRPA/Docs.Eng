# Receive mail (IMAP)

![](<../../../.gitbook/assets/image (57).png>)

Element that reads incoming messages IMAP.

![](<../../../.gitbook/assets/image (293).png>)

Properties

* Server address\*: \[String] Server address
* Port\*: \[Int32] Server port
* Login\*: \[String] Login
* Password\*: \[String] Password
* SSL\*: \[Boolean] Server uses SSL connection
* Folder\*: \[String] Incomming messages folder
* Unread only\*: \[Boolean] Receive only unread messages
* Mark read\*: \[Boolean] Mark received messages as read
* Mark unread\*: \[Boolean] Mark received messages as unread
* Date from\*: \[DateTime?] Message filter date from
* Date to\*: \[DateTime?] Message filter date to
* Receive attachments\*: \[Boolean] Receive attachments
* UIDs: \[System.Collections.Generic.List] Message IDs to receive
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
