# Get processes

![](https://gblobscdn.gitbook.com/assets%2F-M-L9CGkriEo1\_2PfJzA%2F-M5uKwCjVjLLtZ\_jXdZC%2F-M5uNeunURHyG4YW1U6C%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%87%D0%B8%D0%B9\_%D1%81%D1%82%D0%BE%D0%BB\_%D1%81%D0%BF%D0%B8%D1%81%D0%BE%D0%BA%20%D0%BF%D1%80%D0%BE%D1%86\_%D0%B8%D0%BA%D0%BE%D0%BD%D0%BA%D0%B0.png?alt=media\&token=df46fd44-de77-4aea-83fa-26aefa36e93a)

Element that gets list of running processes

![](<../../../.gitbook/assets/image (333).png>)

Properties

&#x20;\- Current user: \[bool] Get only current user processes

&#x20;\- Variable\*: \[List] Variable to store processes list

```
C#
List<System.Diagnostics.Process> proc = LTools.Desktop.DesktopApp.GetProcesses(wf, true);
foreach (var p in proc)
	LTools.Workflow.PrimoApp.AddToLog(wf, p.ProcessName);
	
Python
proc = LTools.Desktop.DesktopApp.GetProcesses(wf, True)
for p in proc:
	LTools.Workflow.PrimoApp.AddToLog(wf, p.ProcessName)
	
JavaScript
var proc = _lib.LTools.Desktop.DesktopApp.GetProcesses(wf, true);
for (var i = 0; i < proc.Count; i++)
	_lib.LTools.Workflow.PrimoApp.AddToLog(wf, proc[i].ProcessName);
```
