# File/folder exists

![](<../../../.gitbook/assets/image (32).png>)

Element that checks for a file or folder

![](<../../../.gitbook/assets/1 (76).png>)

Properties

&#x20;\- Path\*: \[String] Path to a verifiable entity (c:\folder\file.txt)

&#x20;\- Variable\*: \[Boolean] Variable being a test result receiver

&#x20;\- Search for a folder: \[Boolean] Folder search sign

```
C#
bool f = System.IO.File.Exists(@"C:\text.txt");
bool d = System.IO.Directory.Exists(@"C:\Dir");

Python
f = System.IO.File.Exists("C:\\text.txt")
d = System.IO.Directory.Exists("C:\\Dir")

JavaScript
var f = _lib.System.IO.File.Exists("C:\\text.txt");
var d = _lib.System.IO.Directory.Exists("C:\\Dir");
```
