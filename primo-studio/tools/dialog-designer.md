# Dialog designer

Dialog designer creates user dialogs b works with Custom form group elements

![](<../../.gitbook/assets/image (172).png>)

To add new element drag and drop it from Elements panel to your form.

Element properties can be adjusted in Properties panel. The main element property is Name, you may use it to interact with your element.&#x20;

To create new dialog press New form button. To save your form press Save or Save as button. To open your form press Open button. To test your form design press Test form button.

Dialog file can be used in Custom form element. Just supply Custom element File path property with your dialog template file path. To send data to dialog elements use Data (Form group) property. For example, if you have text edit with name "textbox" you may supply it with date using following code:

```
forminput.TextEdit.Add("textbox", "test text")
```

forminput - variable with type LTools.UserInteractions.UserFormResult, "test text" - is a value to send to element.

To get element value you may use Data (Output group) property. For example, the value of text edit named "textbox" can be received with the following code:

```
formdata.TextEdit["textbox"]
```

Dialog window will keep raising until cross-button is pressed or Close form element is called. To get last clicked button name you may use the following code (cross-button returns null):

```
formdata.Action
```
