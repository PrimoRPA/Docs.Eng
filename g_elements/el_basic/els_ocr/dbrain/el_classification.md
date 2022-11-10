# Classify documents

![](<../../../../.gitbook/assets/image (93).png>)

![](<../../../../.gitbook/assets/image (166).png>)



Element that classifies documents using Dbrain server

* Document\*: \[String] Path to document file
* Result: \[LTools.OCR.Model.Dbrain.DbrainClassificationResult] Document processing result

LTools.OCR.Model.FlexiCapture.DbrainClassificationResult - Properties:

* Document \[LTools.OCR.Model.Dbrain.DbrainClassificationDocument]: First processed document
* Documents \[List]: Processed documents array

LTools.OCR.Model.Dbrain.DbrainClassificationDocument - Properties:

* DocType \[string]: Document type
* Page \[Int32]: Page number
* Rotation \[double]: Page rotation
