# Traffic record

The Primo Studio traffic tracking subsystem allows you quickly and easily analyzing the exchange with portals, sites and web services, as well as generating Web requests in scripts based on the data received.

The tracking subsystem is represented by the Traffic Capture, Packet Properties and Traffic Filter panels.

The Traffic Capture panel displays, in chronological order, all requests and responses occurring at the user's workplace in real time. To start recording the traffic, you should click the Start capturing button ![](<../.gitbook/assets/0 (76).png>). As soon as you click the button, the panel table will start to display the requests made from your workplace. The table of requests (queries) displays the following data:

* Result: Request event code
* Protocol: Request protocol type
* Host: Host name
* URL: Remote machine address
* Body: Request (query) body size in bytes
* Caching: Information on caching
* Type of content

Request and response body text can be found by clicking on the + icon in the request header

![](<../.gitbook/assets/1 (134).png>)

To stop recording click the Stop Interception button ![](<../.gitbook/assets/2 (16).png>)

To delete selected requests from the list, click the Delete button ![](<../.gitbook/assets/3 (15).png>)

To clear the list of requests, click the Clear button ![](<../.gitbook/assets/4 (13).png>)

To get more information about a request and a response, you need to select it in the Traffic Capture panel, and then the information about the request will be reflected in the Properties panel of the packet.

![](<../.gitbook/assets/5 (12).png>)

There is information about requests in the upper part of the panel. There is information about responses in the lower part of the panel. The information contained in the panel is divided into the following categories:

* Headers: Information on headers
* Text: Request body text
* Clear: Request/response text in clear text (headers and body)
* JSON: Body data view in the form of JSON
* XML: XML review of body data

There is the Traffic Filter panel necessary for pre-filtering traffic.

![](<../.gitbook/assets/6 (11).png>)

This panel allows:

* Enabling tracking of CONNECT type requests
* Enabling interception of multimedia content requests
* Creating special filters

In the special filter table, you can create filters for certain elements of a request/response based on regular expressions. The filter contains the following elements:

* Result
* Protocol
* Host
* URL
* Content type (request)
* Content type (response)
* Header (request)
* Header (response)
* Body (request)
* Body (response)

For example, to filter requests only to sites with a URL including mail, you need to create a filter with the URL Object and the Expression.\*mail.\*
