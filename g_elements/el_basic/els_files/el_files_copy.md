# Copy file

![](<../../../.gitbook/assets/image (80).png>)

Element copying a file

![](<../../../.gitbook/assets/1 (103).png>)

Properties

&#x20;\- Source\*: \[String] Path to a source file (c:\folder\file1.txt)

&#x20;\- Destination\*: \[String] Path to a destination file (c:\folder\file2.txt)

&#x20;\- Rewrite: \[Boolean] Overwriting sign of a destination file

```
C#
System.IO.File.Copy(@"C:\from", @"C:\to");

Python
System.IO.File.Copy("C:\\from", "C:\\to")

JavaScript
_lib.System.IO.File.Copy("C:\\from", "C:\\to");
```
