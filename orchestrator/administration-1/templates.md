# Templates

The "Templates" page provides information about the created templates that can be used to create robots.

![](<../../.gitbook/assets/image (212).png>)

#### **Woking with templates**

The list of templates can be sorted by each column by clicking on the icon <img src="../../.gitbook/assets/image (284).png" alt="" data-size="line"> .&#x20;

For searching in the list use the search box on the right&#x20;

![](<../../.gitbook/assets/image (199).png>)

You can also customize the display of columns. To do this, you need to click on the icon <img src="../../.gitbook/assets/image (160).png" alt="" data-size="line"> next to the search bar and select the required columns.

![](<../../.gitbook/assets/image (125).png>)

The list of templates can be updated by clicking the icon <img src="../../.gitbook/assets/image (239).png" alt="" data-size="line">  located next to the search bar.

#### Create template

To create the template click the button "Create tempate"&#x20;

![](<../../.gitbook/assets/image (122).png>)

Window for entering data will open. To create template you could fill in the required field "Name" and save the entered data. Optionaly you can set following parameters:

* **Log message types:** selecting a type from the list. Debug - robot debug messages, Error - errors, Network - traffic log when interacting with web services, Info - information about the steps performed,
* **Log format:** Refers to the log of the local robot logs. Selecting a format from the list (csv or text)
* **Flow priority:** The priority of the robot's threads within the operating system (for multi-threaded execution). Selecting a priority from the list.
* **Application priority:** The priority of the robot execution within the operating system (for multithreaded execution. Selecting the priority from the list.
* **Flow count:** The number of parallel executable instances of a given project (load testing). Entering a numerical value.
* **Start index flow:** The identifier of the first stream, further streams are identified with a step plus one. Entering a numerical value.
* **Min threads:** The minimum size of the application thread pool. It is recommended to set more than the total number of threads. Entering a numerical value.
* **Log custom to file:** The need to write logs of user messages to a file. Set by switch.
* **No control:** The need to write logs to the console. Set by switch.
* **Log to file:** The need to write logs to a file. Set by switch.

![](<../../.gitbook/assets/image (263).png>)
