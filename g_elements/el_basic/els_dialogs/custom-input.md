# Custom input

![](https://gblobscdn.gitbook.com/assets%2Fprimo-rpa%2F-M-fe71a7oWXLrVv-9kL%2F-M-feFTugXUvuoGIT1BY%2F0.png?generation=1581280463668702\&alt=media)

Element that displays the user data entry window.

![](../../../.gitbook/assets/Custom\_input.png)

Properties

&#x20;\- URL\*: \[String] dialog URL (For example: http://myserver/dialog.html или file:///c:/dialog.html)

&#x20;\- Width\*: \[Int32] Dialog width

&#x20;\- Heght\*: \[Int32] Dialog height

&#x20;\- Result: \[String] data obtained from the dialog

Example of dialog page:

```
<!DOCTYPE html>
<html lang="en">
 <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <title>Primo Dialog</title>
  </head>
  <body>      
          Имя:<br>
          <input type="text" id="First_Name"><br>
          Фамилия:<br>
          <input type="text" id="Last_Name"><br>
          Возраст:<br>
          <input type="text" id="Age"><br>
          <button onclick="SubmitValues()">Отправить</button>


          <script type="text/javascript">
          function SubmitValues(){
            var First_Name = document.getElementById("First_Name").value;
            var Last_Name = document.getElementById("Last_Name").value;
            var Age = document.getElementById("Age").value;
            window.external.finished(First_Name + "," + Last_Name + "," + Age);
            return true;
          }            
          </script>
  </body>
  </html>

```

To pass data to the robot you need to call the function window.external.finished&#x20;
