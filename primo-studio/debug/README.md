# Process execution and debugging

Before you start debugging you should choose desired robot edition: Standard or Enterprise in Studio main panel.

In order to execute a process, you should click the "Playback" button of the Process menu or the corresponding button of the Actions panel ![](<../../.gitbook/assets/0 (48).png>)

To start debugging a process you should click the "Debug" button of the Process menu or the corresponding button of the Actions panel ![](<../../.gitbook/assets/1 (44).png>)

You may also start debugging from any element. To do so just right-click the desired element and press "Execute from element" menu item

![](<../../.gitbook/assets/image (268).png>)

After pressing the button, an instance of the robot is launched, which will immediately execute the current process. The Console panel is available for viewing process messages.

![](<../../.gitbook/assets/2 (13).png>)

There are the following buttons on the Console panel.

![](<../../.gitbook/assets/3 (3).png>) Follow the filling of the console: the console text will always focus on the last message received.

![](<../../.gitbook/assets/4 (2).png>) Clear the console: clears the console contents

The console contains DEBUG, INFO, ERROR and NETWORK filters. These filters are responsible for collecting messages of the corresponding type.

The progress of a script is displayed with the following icon ![](<../../.gitbook/assets/5 (6).png>). This icon indicates an element that is being executed at a given moment.

To disable (ignore) an element at runtime, click the symbol <img src="../../.gitbook/assets/4 (14).png" alt="" data-size="line"> in the header of the element. After this setting  the element will not be executed during the script run.

The start of Debugging differs in that there is no stop at Breakpoint during startup. To set a breakpoint, click ![](<../../.gitbook/assets/6 (1).png>) symbol in the header of the necessary element.

![](<../../.gitbook/assets/8 (1).png>)

If a process reaches an element with a breakpoint during debugging, the process will be stopped until you press one of the following buttons: "Take a Step" ![](<../../.gitbook/assets/9 (1).png>) or "Resume the Process" ![](../../.gitbook/assets/10.png). These buttons are located in the Process menu and on the Actions panel. The "Take a Step" button allows moving to the next element, after which a process is stopped again. The "Resume the Process" button resumes the free execution of a process until the next breakpoint.

To force the completion of a process you should press the "Stop Debugging" button in the Process menu or the corresponding button of the Actions panel ![](../../.gitbook/assets/11.png).

The states of variables will be displayed in the Current value column of the Variables panel.

![](<../../.gitbook/assets/12 (3).png>)

For easy viewing the current value you can clik the View button![](../../.gitbook/assets/variable.png), then a window will be displayed to view the value in JSON format.

![](../../.gitbook/assets/variable\_view.png)

You can work with variables and expressions on the Observation panel (by functionality corresponding to the Watch panel of classic development environments).

![](<../../.gitbook/assets/13 (1).png>)

The table of the panel shows the calculated expression, the data type of the calculation result and the calculation result. To create a new observation, you should press the "Create an Observation" button ![](../../.gitbook/assets/14.png) and enter the text of the calculated expression in the appeared window.

![](../../.gitbook/assets/15.png)

To update the calculation results, press the "Update" button ![](../../.gitbook/assets/16.png) of the corresponding observation.

To edit the calculated expression, you can either edit the text right in the table cell or open the editing window by double-clicking on the desired observation.

To delete an observation, you can select the observation in the table and either click the "Delete the Observation" button ![](<../../.gitbook/assets/17 (1).png>), or press the "Delete" key.

To debug either Standard or Enterprise robot edition choose the desired edition in Studio main menu
