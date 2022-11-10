# Move file

![](<../../../.gitbook/assets/image (83).png>)

Element that moves a file

![](<../../../.gitbook/assets/1 (130).png>)

Properties

&#x20;\- Source\*: \[String] Path to a source file (c:\folder\file1.txt)

&#x20;\- Destination\*: \[String] Path to a destination file (c:\folder\file2.txt)

&#x20;\- Rewrite: \[Boolean] Sign of destination file rewriting

```
C#
System.IO.File.Move(@"C:\from", @"C:\to");

Python
System.IO.File.Move("C:\\from", "C:\\to")

JavaScript
_lib.System.IO.File.Move("C:\\from", "C:\\to");
```
