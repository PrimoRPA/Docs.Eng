# Image exists

![](<../../../.gitbook/assets/0 (58).png>)

Element that searches for a given image on the screen.

In the case where the value of a sought image is not specified, the image is taken from the screenshot of element.

![](<../../../.gitbook/assets/1 (11).png>)

Properties:

&#x20;\- Image sought: \[System.Drawing.Bitmap] Raster of the image you are searching for

&#x20;\- Accuracy: \[Double] Matching accuracy of an image (raster) (from 0 to 1 %)

&#x20;\- Coordinates: \[System.Drawing.Rectangle] Coordinates of an image found

&#x20;\- Timeout\*: \[Int32] Maximum waiting time for process completion (ms)
