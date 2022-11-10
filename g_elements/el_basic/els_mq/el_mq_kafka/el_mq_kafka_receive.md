# Read messages

![](<../../../../.gitbook/assets/image (65).png>)

Element that read messages from ActiveMQ server queue.

![](../../../../.gitbook/assets/queues\_read\_message.png)

Properties

&#x20;\- Server address\*: \[String] ActiveMQ server address (tcp://myserver:61616/)

&#x20;\- Login: \[String] Login

&#x20;\- Password: \[String] Password

&#x20;\- Destination type\*: destination type (queue, topic)

&#x20;\- Topic/queue\*: \[String] Topic/queue name

&#x20;\- Message array: \[System.Collections.Generic.List\<LTools.Network.MQ.AMQMessage>] Array of received messages

&#x20;\- Wait for message: \[Boolean] Flag for waiting for a new message in queue

&#x20;\- Time-out\*: \[Int32] Max process await timeout (ms)

\- GroupID: \[String] Group ID

LTools.Network.MQ.KafkaMessage - Properties:

&#x20;\- Text: \[String] Message text (if type eq. TEXT)

&#x20;\- Timestamp: \[DateTime] Message date and time
