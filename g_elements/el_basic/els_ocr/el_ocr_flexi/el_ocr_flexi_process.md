# Process documents

Element that processes documents using FlexiCapture server

![](<../../../../.gitbook/assets/image (203).png>)

* Project\*: \[String] Project name
* Batch\*: \[String] Batch name
* Document: \[String] Path to document file
* Documents array: \[List] Array of paths to document files
* Delete batch: Delete batch on finish
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)
* Result: \[LTools.OCR.Model.FlexiCapture.RecognitionResults] Document processing result

LTools.OCR.Model.FlexiCapture.RecognitionResults - Properties:

* Items \[List: Processing results array

LTools.OCR.Model.FlexiCapture.RecognitionDocument - Properties:

* \[string (template name)] \[LTools.OCR.Model.FlexiCapture.RecognitionResult]: Template processing result
* Items \[List]: Processed templates array
* Xml \[string]: Raw server data

LTools.OCR.Model.FlexiCapture.RecognitionResult - Properties:

* \[string (field name)] \[string]: Field data
* \[int (index)] \[KeyValuePair?]: Field data (key - field name, value - field data)
* Fields \[Dictionary]: Fields array (key - field name, value - field data)
* Tables \[Dictionary>>]: Tables array (key - table name, value - tables array)
* TemplateName \[string]: Template name
* State \[string]: Processing result state
