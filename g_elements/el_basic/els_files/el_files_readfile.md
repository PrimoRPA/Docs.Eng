# Read file

![](<../../../.gitbook/assets/image (16).png>)

Element that reads the content file.

![](<../../../.gitbook/assets/1 (87).png>)

Properties

&#x20;\- Path\*: \[String] Path to a file to be read (c:\folder\file.txt)

&#x20;\- Variable (text): \[String] Variable that receives text data from a file

&#x20;\- Variable (array): \[byte\[]] Variable that accepts binary data in a file

&#x20;\- Variable (image): \[System.Drawing.Bitmap] Variable that accepts image data from a file

&#x20;\- Encoding: \[String] Encoding used in a file (utf-8) 'https://docs.microsoft.com/ru-ru/dotnet/api/system.text.encoding'

```
C#
string txt = System.IO.File.ReadAllText(@"C:\text.txt");
byte[] bytes = System.IO.File.ReadAllBytes(@"C:\bytes.txt");

Python
txt = System.IO.File.ReadAllText("C:\\text.txt")
bytes = System.IO.File.ReadAllBytes("C:\\bytes.txt")

JavaScript
var txt = _lib.System.IO.File.ReadAllText("C:\\text.txt");
var bytes = _lib.System.IO.File.ReadAllBytes("C:\\bytes.txt");
```
