# IElementInfo

LTools.WebBrowser.Model.IElementInfo - the object that contains a link to a control element.

| Свойство    | Тип                  | Описание          |
| ----------- | -------------------- | ----------------- |
| BaseElement | Object               | Base element      |
| ID          | String               | ID                |
| TagName     | String               | Tag name          |
| ClassName   | String               | Class             |
| Name        | String               | Name              |
| Value       | String               | Value             |
| InnerText   | String               | Text              |
| ListItems   | List\<string>        | List elements     |
| ListCurrent | List\<string>        | Selected list element |
| Attributes  | List\<ElementAttribute> | Element attribites |
| SearchPattern | ElementSearchPattern | Search pattern  |
| Index       | Int                  | Index             |
| X           | Int                  | X                 |
| AbsoluteX   | Int                  | X                 |
| Y           | Int                  | Y                 |
| AbsoluteY   | Int                  | Y                 |
| Width       | Int                  | Width             |
| Height      | Int                  | Height            |
| Visible     | Boolean              | Element visibility |
| IsChecked   | Boolean              | Selected checkbox attribute |
| BoundingRect | [Rectangle](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.rectangle?view=net-8.0) | Element boundaries |
| OuterHtml    | String              | HTML               |
