# Save attachment

![](<../../../../.gitbook/assets/MSExchange-SaveAttach.png>)


Component that saves email attachments.

##Properties

| Property     | Type                                                                    | Description                        |
| ------------ | ----------------------------------------------------------------------- | ---------------------------------- |
| File path    | String                                                                  | Path to the file (c:\folder\files.ext) |
| Attachment   | [LTools.Office.Model. OMailAttachment](../data-types/omailattachment.md) | Email attachment                  |

{% tabs %}
{% tab title="C#" %}
```csharp
app.SaveAttachment(att, "C\\file");
```
{% endtab %}

{% tab title="Python" %}
```python
app.SaveAttachment(att, "C\\file")
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
app.SaveAttachment(att, "C\\file");
```
{% endtab %}
{% endtabs %}
