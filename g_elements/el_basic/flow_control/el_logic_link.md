# Process link

![](<../../../.gitbook/assets/image (56).png>)

Element that performs the process specified in the link.

![](<../../../.gitbook/assets/1 (120).png>)



Properties

* Process path\*: \[String] Path to a process file (c:\folder\file.ltw)
* Mapping\*: \[LTools.Common.Model.VariablesMapping] Arguments mapping
* Run in SnadBox: Execute process in Windows SandBox
* Close: Close SandBox on finish
* Start timeout\*: \[Int32] SandBox start timeout
* Finish timeout\*: \[Int32] Robot finish timeout (0 - infinite)
* Parallel: Start SandBox parallel to main process

LTools.Common.Model.VariablesMapping

Properties:

* \[String] \[Scripting.Model.ScriptVariable]: Variable reference
* ThrowOnKeyNotExists \[Boolean]: Throw exception if argument does not exist

Methods:

* AddMapping(string, Scripting.Model.ScriptVariable): Add new mapping (argument, variable)
* DeleteMapping(string): Delete mapping (argument)

```
C#
//Creating arguments
List<LTools.Workflow.Model.SequenceLinkArg> args = new List<LTools.Workflow.Model.SequenceLinkArg>();
args.Add(new LTools.Workflow.Model.SequenceLinkArg() { Name = "arg1", Value = "val1" });
//Process invoke
args = LTools.Workflow.Elements.WFSequenceLink.CallWorkflow(wf, @"C:\Project\Process.ltw", args);
//Getting arguments
string ret = args.Where(it => it.Name == "arg1").FirstOrDefault().Value as string;

Python
#Creating arguments
args = List[LTools.Workflow.Model.SequenceLinkArg]()
args.Add(LTools.Workflow.Model.SequenceLinkArg("arg1", "val1"))
#Process invoke
args = LTools.Workflow.Elements.WFSequenceLink.CallWorkflow(wf, "C:\\Project\\Process.ltw", args)
#Получаем аргументы
ret = ret[0].Value

JavaScript
let host = new _lib.Microsoft.ClearScript.HostFunctions();
//Creating arguments
let args = host.newObj(_lib.System.Collections.Generic.List(_lib.LTools.Workflow.Model.SequenceLinkArg));
args.Add(new _lib.LTools.Workflow.Model.SequenceLinkArg("arg1", "val1"));
//Process invoke
args = _lib.LTools.Workflow.Elements.WFSequenceLink.CallWorkflow(wf, "C:\\Project\\Process.ltw", args, false);
//Getting arguments
let ret = args[0];
```
