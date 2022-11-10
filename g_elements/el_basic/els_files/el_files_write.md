# Write file

![](<../../../.gitbook/assets/image (22).png>)

Element rewriting the content of a file

![](<../../../.gitbook/assets/1 (129).png>)

Properties

&#x20;\- Encoding: \[String] Encoding used in a file (utf-8) 'https://docs.microsoft.com/ru-ru/dotnet/api/system.text.encoding'

&#x20;\- File path\*: \[String] Path to a file to be written (c:\folder\file.txt)

&#x20;\- Text: \[String] Text to be written to a file

&#x20;\- Array: \[byte\[]] Binary data recorded in a file

&#x20;\- Image: \[System.Drawing.Bitmap] Image to be written to a file

```
C#
System.IO.File.WriteAllLines(@"C:\text.txt", new List<string>() { "New text" });
System.IO.File.WriteAllText(@"C:\text.txt", "New text");
System.IO.File.WriteAllBytes(@"C:\bytes.txt", new byte[0]);

Python
System.IO.File.WriteAllLines("C:\\text.txt", List[String](["New text"]));
System.IO.File.WriteAllText("C:\\text.txt", "New text");
System.IO.File.WriteAllBytes("C:\\bytes.txt", Array[Byte]([]));

JavaScript
var host = new _lib.Microsoft.ClearScript.HostFunctions();
var items = host.newObj(_lib.System.Collections.Generic.List(_lib.System.String));
items.Add("New text");
_lib.System.IO.File.WriteAllLines("C:\\text.txt", items);
_lib.System.IO.File.WriteAllText("C:\\text.txt", "New text");
var bytes = host.newObj(_lib.System.Collections.Generic.List(_lib.System.Byte));
_lib.System.IO.File.WriteAllBytes("C:\\bytes.txt", bytes.ToArray());
```
