# Working with workflows

There are several ways to create a workflow:

1\)  you could select the type "Workflow" when creating a process.

![](../.gitbook/assets/new\_process.png)

2\) or add  Workflow element <img src="../.gitbook/assets/image (334).png" alt="" data-size="line"> to sequence or to workflow

Workflow may include the following elements:

* Workflow start
* Sequence
* Decision
* Workflow
* State

They are in the Workflow group of the Elements panel.&#x20;

The "Workflow start" element is always present and indicated by the green circle symbol.

![](<../.gitbook/assets/1 (60).png>)

The Sequence element is a rectangle comprising a standard sequence. To switch to a stored sequence, double-click the Sequence element.

![](<../.gitbook/assets/image (237).png>)

To return to a Chart you should press the "Return" button in the upper left corner of a Chart.

![](<../.gitbook/assets/3 (8).png>)

To add a sequence, drag it from the Elements panel

![](<../.gitbook/assets/2 (15).png>)

The decision-making element is a blue diamond symbol, which serves to branch out a process (similar to the Switch structure of classical programming languages). To create a condition, it is necessary to specify a calculated expression in the "Condition" property of the Properties panel.

![](<../.gitbook/assets/image (249).png>)

To add a decision, drag it from Elements panel

![](<../.gitbook/assets/0 (95).png>)

The Workflow element is a rectangle with a workflow inside

![](<../.gitbook/assets/image (317).png>)

To add a Workflow, drag it from Element panel&#x20;

![](<../.gitbook/assets/image (334).png>)

The State element is a rectangle with  process states inside. You can make transitions between them.

![](<../.gitbook/assets/image (332).png>)

To add a State, drag it from Element panel

![](<../.gitbook/assets/image (313).png>)

To set up a Workflow use the workflow action panel

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M7MR9lqwDg8kI\_0mC5C%2F-M7MaLpxhRrzbJCsGWot%2Fimage.png?alt=media\&token=051054df-fe5d-41c7-8a40-1fabafa1a98d)

To create connections between elements, click the Connection button <img src="../.gitbook/assets/image (139).png" alt="" data-size="line"> on the workflow action panel. Then click on the green square on any edge of the element (if you need to specify starting point) or hold down the mouse button on the element (the element is highlighted with a green frame and the location of the arrow start will be set automatically) and drag arrow to the green square or green frame of another element.

![](<../.gitbook/assets/image (298).png>)

![](<../.gitbook/assets/image (142).png>)

To return to the usual cursor and work with other elements, press Pointer <img src="../.gitbook/assets/image (232).png" alt="" data-size="line"> button on the workflow action panel.

Diagram connection can be of three shapes:

![Angled](<../.gitbook/assets/image (49).png>)

![Straight](<../.gitbook/assets/image (111).png>)

![Curved](<../.gitbook/assets/image (34).png>)

Connection shape can be changed through it's properties and becomes default shape for new connections.

To branch out a process, you must set the conditions to be checked. To do this, you should select the arrow coming from the lower square of the Decision element and specify the value corresponding to the decision made in the "Equation Result" property. The arrow without the specified result will be the default solution.

![](<../.gitbook/assets/image (225).png>)

You can use the Grid and  Snap to grid  functions for element’s easy alignment.&#x20;

Press the Grid  button on the workflow action panel to turn the grid on/off. When this feature is enabled, the lines appear in the working area, making element’s alignment more convenient.

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M7MkG34UiiPCxiv8anD%2F-M7NR6zDa5bLAYrs-F-X%2Fimage.png?alt=media\&token=68578ce5-3599-4646-93ae-2615ba3ba646)

You can also snap elements to the grid by pressing Snap to grid button on the workflow action panel. When this feature is enabled, you can move elements by the grid.

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M7MkG34UiiPCxiv8anD%2F-M7NRBxszvZNX0epYbbZ%2Fimage.png?alt=media\&token=eb6c201c-9385-44b7-9275-8f8545f3ed56)

Also guide lines are displayed when moving elements for it's easy alignment.

Otherwise, the Workflow functions fully correspond to the Sequence functions.
