---
title: Access HTML Forms
module: 4
jotted: true
---

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
  <button class="tablinks" onclick="openTab(event, 'Create')">Create a HTML Form</button>
 <button class="tablinks" onclick="openTab(event, 'Display')">Retrieve Data</button>
  
 
</div>

<div id="Overview" class="tabcontent" style="display:block">
PHP and HTML Forms
<p>
Keep in mind that PHP uses regular HTML forms.  There is no code behind, but we can still access the data.</p>
</div>

<div id="Create" class="tabcontent">
<div class="tabhtml" markdown="1">
Create HTML Form
<p>
How do we create a basic input form?</p>

```html
<html>
    <head>
        <title>Login!</title>
    </head>
    <body>
        <form action="processlogin.php" method="POST">
        <table>
            <tr>
                <td>
                    Username:
                </td>
                <td>
                    <input type="text" name="username">
                </td>
            </tr>
            <tr>
                <td>
                    Password:
                </td>
                <td>
                    <input type="text" name="pwd">
                </td>
            </tr>
            <tr>
                <td colspan="2">
                    <input type="submit" value="Submit">
                </td>
            </tr>
        </table>
        </form>
    </body>
</html>
```
</div>
</div>

<div id="Display" class="tabcontent" markdown="1">
<div class="tabhtml" markdown="1">
Access Data with PHP

<p>What is the difference between $_GET and $_POST?</p>

POST puts all the data in hidden fields while GET puts it into the QueryString.

```php
<?php

    // This makes sure it's a post action
    if($_SERVER["REQUEST_METHOD"] == "POST")
    {
        // gets the username from the form by looking at the name attribute
        // $username is how variables are created - ($) before the variable name
        // not strongly typed
        $username = $_POST["username"];
        // gets the pwd by looking at the pwd attribute
        $pwd = $_POST["pwd"];
    }
?>
```
</div>
</div>

