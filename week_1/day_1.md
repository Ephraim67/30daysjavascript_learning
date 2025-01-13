## Hello World

The ```"script"``` tag:

JavaScript programs can be inserted almost anywhere into an HTML document using the <script> tag.
```HTML
<!DOCTYPE HTML>
<html>
  <body>
    <p>
      The body of the message    </p>
    <script>
      alert('Hello, world');
    </script>
    <p>The message ends here</p>
  </body>
</html>
```

## Moder Markup
* The ```<script>``` tag has a few attributes that are rarely used 
* The type attribute: ```<script type=…>```: used for old browsers
* The language attribute: ```<script language=…>:``` This attribute was meant to show the language of the script. 
* This attribute no longer makes sense because JavaScript is the default language. There is no need to use it.



## Summary
* We can use a ```<script>``` tag to add JavaScript code to a page.
* The type and language attributes are not required.
* A script in an external file can be inserted with ```<script src="path/to/script.js"></script>```.
