# Process documents

![](<../../../../.gitbook/assets/image (8).png>)

![](<../../../../.gitbook/assets/image (158).png>)



Element that processes documents using Dbrain server

* Document\*: \[String] Path to document file
* Result: \[LTools.OCR.Model.Dbrain.DbrainRecognitionResult] Document processing result

LTools.OCR.Model.FlexiCapture.DbrainRecognitionResult - Properties:

* Document \[LTools.OCR.Model.Dbrain.DbrainRecognitionDocument]: First processed document
* Documents \[List]: Processed documents array
* ThresholdOKMin \[Int32]: Minimum correct results range
* ThresholdWarnMin \[Int32]: Minimum warning results range
* HasWarnings \[Boolean]: Has warninigs
* HasErrors \[Boolean]: Has errors

LTools.OCR.Model.Dbrain.DbrainRecognitionDocument - Properties:

* \[string (имя шаблона)] \[LTools.OCR.Model.Dbrain.DbrainRecognitionItem]: Template processing result
* Items \[List]: Processed templates array
* DocType \[string]: Document type

LTools.OCR.Model.Dbrain.DbrainRecoginitionItem - Properties:

* Name \[String]: Element name
* Text \[String]: Element text
* Confidence \[double]: Confidence
