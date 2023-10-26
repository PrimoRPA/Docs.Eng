# Save attachment

![](<../../../../.gitbook/assets/Lotus-SaveAttach.png>)


Component that saves email attachments.

Properties:

| Property     | Type                                                                    | Description                        |
| ------------ | ----------------------------------------------------------------------- | ---------------------------------- |
| Filepath     | String                                                                  | Path to the file (c:\folder\files.ext) |
| Attachment   | [LTools.Office.Model. OMailAttachment](../datatypes/omailattachment.md) | Email attachment                   |

{% tabs %}
{% tab title="C#" %}
```csharp
app.SaveAttachment(att, "C:\\file.txt");
```
{% endtab %}

{% tab title="Python" %}
```python
app.SaveAttachment(att, "C:\\file.txt")
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
app.SaveAttachment(att, "C:\\file.txt");
```
{% endtab %}
{% endtabs %}
