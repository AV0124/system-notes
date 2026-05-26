# Natas0 | OverTheWire Natas Wargame

## Enetering Credentials
- natas0
- natas0

## Challenge
Looking for the password of Natas1, but the page seems to be empty.

## Solution
A webpage is never empty. Right-Clicking anywhere on a page reveals the context menu, which gives the option to Inspect the page, revealing hidden properties.

The 'Elements' section of the Inspect panel shows us the HMTL index/source for the page. For this challenge, I found the index to be:

~~~
<html>
<head>
<!-- This stuff in the header has nothing to do with the level -->
<link rel="stylesheet" type="text/css" href="http://natas.labs.overthewire.org/css/level.css">
<link rel="stylesheet" href="http://natas.labs.overthewire.org/css/jquery-ui.css" />
<link rel="stylesheet" href="http://natas.labs.overthewire.org/css/wechall.css" />
<script src="http://natas.labs.overthewire.org/js/jquery-1.9.1.js"></script>
<script src="http://natas.labs.overthewire.org/js/jquery-ui.js"></script>
<script src=http://natas.labs.overthewire.org/js/wechall-data.js></script><script src="http://natas.labs.overthewire.org/js/wechall.js"></script>
<script>var wechallinfo = { "level": "natas0", "pass": "natas0" };</script></head>
<body>
<h1>natas0</h1>
<div id="content">
You can find the password for the next level on this page.

<!--The password for natas1 is 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq -->
</div>
</body>
</html>
~~~

The password was hidden in the body of the index as a comment.

Takeaway: Webpages can be inspected for more information.