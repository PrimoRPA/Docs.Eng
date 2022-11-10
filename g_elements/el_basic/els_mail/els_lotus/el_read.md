# Read mail

Element that read mail from Lotus Notes.

![](<../../../../.gitbook/assets/image (296).png>)

Properties:

* Folder\*: \[String] Message folder
* Attachments: Read attachments
* Quantity: \[Int32] Quantity of messages to read
* Lotus: \[LTools.Network.Model.EMail.LotusInst] Lotus connection
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)
* Messages: \[List] Variable to store messages

LTools.Office.Model.OMailMessage - Properties:

* ID: \[String] Message identifier
* Body: \[String] Message body text
* MailFormat: \[LTools.Office.Model.OMailMessage.MailFormats] Message format
* Subject: \[String] Message body
* From: \[String] From
* SendTo: \[String] To (address)
* To: \[List] To (reply)

Tools.Office.Model.OMailMessage.MailFormats - Properties:

* PLAIN: Plain text
* RICHTEXT: Rich Text
* HTML: HTML

LTools.Office.Model.OMailAttachment - Properties:

* FileName: \[String] File name
* DisplayName: \[String] Display file name
* Data: \[byte\[]] Content
