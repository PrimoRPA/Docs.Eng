# OMailAttachment

LTools.Office.Model.OMailAttachment - the model describes email attachments.

| Property    | Type    | Description       |
| ----------- | ------- | ---------------- |
| FileName    | String  | Attachment file name. When using elements of MS Exchange parameter `OMailAttachment.FileName` does not always display the file name correctly (may be blank). If the `.FileName` is blank, we recommend using `.DisplayName`  |
| DisplayName | String  | Attachment display name |
| Data        | byte\[] | File contents     |
