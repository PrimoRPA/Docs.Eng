# File search

![](<../../../.gitbook/assets/image (53).png>)

Searches for files and directories.

![](<../../../.gitbook/assets/image (311).png>)

Properties:

&#x20;\- Path\*: \[String] Files search path (C:\Directory)

&#x20;\- Pattern: \[String] File search pattern (_._)

&#x20;\- Variable\*: \[List] Variable to store found files paths

&#x20;\- Search inside folders: Search inside folders

```
C#
string[] files = System.IO.Directory.GetFiles(@"C:\", "*.txt", System.IO.SearchOption.AllDirectories);

Python
files = System.IO.Directory.GetFiles("C:\\", "*.txt", System.IO.SearchOption.AllDirectories)

JavaScript
var files = _lib.System.IO.Directory.GetFiles("C:\\", "*.txt", _lib.System.IO.SearchOption.AllDirectories);
```
