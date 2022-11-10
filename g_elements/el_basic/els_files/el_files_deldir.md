# Delete file/folder

![](<../../../.gitbook/assets/image (111).png>)

Element deleting a file

![](<../../../.gitbook/assets/1 (109).png>)

Properties

&#x20;\- Path\*: \[String] Path to a file to be deleted (c:\folder\file.txt)

```
C#
System.IO.File.Delete(@"C:\text.txt");
System.IO.Directory.Delete(@"C:\Dir");

Python
System.IO.File.Delete("C:\\text.txt")
System.IO.Directory.Delete("C:\\Dir")

JavaScript
_lib.System.IO.File.Delete("C:\\text.txt");
_lib.System.IO.Directory.Delete("C:\\Dir");
```
