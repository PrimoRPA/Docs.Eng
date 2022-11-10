# Append line

![](<../../../.gitbook/assets/image (96).png>)

Element that adds a string to the end of the file.

![](<../../../.gitbook/assets/1 (79).png>)

Properties

&#x20;\- Coding: \[String] Encoding used in a file (utf-8) 'https://docs.microsoft.com/ru-ru/dotnet/api/system.text.encoding'

&#x20;\- Path to a file\*: \[String] Path to a file for recording (c:\folder\file.txt)

&#x20;\- Text\*: \[String] Text of a recordable string

```
C#
System.IO.File.AppendAllLines(@"C:\text.txt", new List<string>() { "New text" });
System.IO.File.AppendAllText(@"C:\text.txt", "New text");

Python
System.IO.File.AppendAllLines("C:\\text.txt", List[String](["New text"]))
System.IO.File.AppendAllText("C:\\text.txt", "New text")

JavaScript
var host = new _lib.Microsoft.ClearScript.HostFunctions();
var items = host.newObj(_lib.System.Collections.Generic.List(_lib.System.String));
items.Add("New text");
_lib.System.IO.File.AppendAllLines("C:\\text.txt", items);
_lib.System.IO.File.AppendAllText("C:\\text.txt", "New text");
```
