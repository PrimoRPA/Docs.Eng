# ActiveMQ

![](<../../../../.gitbook/assets/image (37).png>)

Element that read messages from ActiveMQ server queue.

![](../../../../.gitbook/assets/queues\_read\_message.png)



Properties

&#x20;\- Server address\*: \[String] ActiveMQ server address (tcp://myserver:61616/)

&#x20;\- Login: \[String] Login

&#x20;\- Password: \[String] Password

&#x20;\- Destination type\*: Destination type

&#x20;\- Topic/Queue\*: \[String] Topic/queue name

&#x20;\- Messages array: \[System.Collections.Generic.List] Received messages array

&#x20;\- Delete messages: \[Boolean] Delete message after receive

&#x20;\- Time-out\*: \[Int32] Max process await timeout (ms)

LTools.Network.MQ.AMQMessage - Properties:

&#x20;\- MessageID: \[String] Message ID&#x20;

&#x20;\- MessageType: \[LTools.Network.MQ.AMQMessageTypes] Message type

&#x20;\- Text: \[String] Message text (if type eq. TEXT)

&#x20;\- Object: \[Object] Message object (if type eq. OBJECT)

&#x20;\- CorrelationID: \[String] Correlation ID

&#x20;\- GroupID: \[String] Group ID

&#x20;\- Timestamp: \[DateTime] Message date and time

