# Create mapping

![](<../../../../.gitbook/assets/image (242).png>)

Maps variables to arguments of a sequence being called.

![](../../../../.gitbook/assets/Data\_create\_mapping.png)

Properties

&#x20;\- Variable\*: \[LTools.Common.Model.VariablesMapping] Variable to store mapping

&#x20;\- Assignments\*: \[System.Collections.Generic.Dictionary] Map collection (Argument name - Variable name)

LTools.Common.Model.VariablesMapping

Properties:

&#x20;\- \[String] \[Scripting.Model.ScriptVariable]: Variable reference

&#x20;\- ThrowOnKeyNotExists \[Boolean]: Throw exception if argument does not exist

Methods:

&#x20;\- AddMapping(string, Scripting.Model.ScriptVariable): Add new mapping (argument, variable)

&#x20;\- DeleteMapping(string): Delete mapping (argument)

Addition:

You can also create mapping in the code, using, for example, the C # Script element.&#x20;

{% content-ref url="../../els_prog/el_prog_cs.md" %}
[el\_prog\_cs.md](../../els\_prog/el\_prog\_cs.md)
{% endcontent-ref %}

In this case, the script may be like:

```
map.DeleteMapping("arg1");
map.AddMapping("arg2", new ScriptVariable() { Value = var1, Name = "var1" });
```

