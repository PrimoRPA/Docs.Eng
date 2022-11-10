# Tree

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5WyIL3Y1LiEBixxJle%2F-M5X3tEU7kL-sxCEsz4u%2FSAP\_%D0%B4%D0%B5%D1%80%D0%B5%D0%B2%D0%BE\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=5c7ec601-3802-40c5-8a7b-76a017135db2)

Element which gets reference to UI component Tree.

![](../../../.gitbook/assets/SAP\_tree.png)

Properties:

Element which gets reference to UI component Tree.

Properties:

* Control ID: \[String] Control ID
* Control: \[LTools.SAP.Model.SAPUIItem] Control reference
* Tree: \[LTools.SAP.Model.SAPUITree] Variable that stores tree reference
* Variable: \[LTools.SAP.Model.SAPUITree] Variable to store tree reference
* Nodes: \[List] Tree nodes
* Select: \[String] Select tree node
* Double click: \[String] Node double click
* Expand: \[String] Expand node
* Collapse: \[String] Collapse node
* Time-out\*: \[Int32] Maximum waiting time for process completion (ms)

LTools.SAP.Model.SAPUITree:&#x20;

* \[SAPFEWSELib.ISapTreeTarget] Element - Element reference;&#x20;
* \[String] Id - Element ID;&#x20;
* \[List\<String>] ColumnTitles - Column titles;&#x20;
* \[List\<String>] ColumnNames - Column names;&#x20;
* \[List\<LTools.SAP.Model.SAPUITreeNode>] Nodes - Tree nodes;&#x20;
* SelectNode(String key - node key) - Select tree node;&#x20;
* DoubleClickNode(String key - node key) - Perform node double click.

LTools.SAP.Model.SAPUITreeNode:&#x20;

* \[String] Key - Node key;&#x20;
* \[String] Text - Node text.

```
C#
LTools.SAP.SapApp app = LTools.SAP.SapApp.Init(wf);
LTools.SAP.Model.SAPUITree tree = app.Tree("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
tree.ExpandNode(tree.Nodes[0].Key);

Python
app = LTools.SAP.SapApp.Init(wf);
tree = app.Tree("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell")
tree.ExpandNode(tree.Nodes[0].Key)

JavaScript
var app = _lib.LTools.SAP.SapApp.Init(wf);		
var tree = app.Tree("/app/con[0]/ses[0]/wnd[0]/usr/cntlIMAGE_CONTAINER/shellcont/shell/shellcont[0]/shell");
tree.ExpandNode(tree.Nodes[0].Key);
```
