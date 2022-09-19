---
title: PHP Simple Page
module: 4
---

# Create a PHP Page

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
  <button class="tablinks" onclick="openTab(event, 'Examples')">Examples</button>
  
 
</div>


<div id="Overview" class="tabcontent" style="display:block">
<div class="tabhtml" markdown="1">
You can use VS Code, Atom or any other editor to create a simple PHP file.  Just remember, it must start with:

```php
    <?
```
and end with
```php
    ?>
```
</div>
</div>
<div id="Examples" class="tabcontent">
<div class="tabhtml" markdown="1">
In the previous example, calling phpinfo() displayed which version of php was installed on the machine.

One can also put in the following:

```php
    <? echo 'Hello world!' ?>
```

Finally, one can also inject php code inside of HTML like this.

```html
<html>
 <head>
  <title>PHP Test</title>
 </head>
 <body>
 <?php echo '<p>Hello World</p>';
 phpinfo();
 ?> 
 </body>
</html>
```
</div>
</div>
