# Natas1 | OverTheWire Natas Wargames

### Entering Credentials
- natas1
- 0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq

### Challenge
The webpage is yet again blank. Trying to open Inspect panel from the context menu is not possible as the webpage is programmed to block right-clicking. 
We must find another way.

### Solution
There is another way to open the Inspect panel, and it is honestly a preferred, much faster way.
Pressing Ctrl + Shift + I opens the Inspect panel directly. 

In the Elements section I found this:
~~~
<div id="content">
You can find the password for the
next level on this page, but rightclicking has been blocked!

<!--The password for natas2 is TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI -->
</div>
~~~

A Division container with a commented password!

## Takeaway: Using keybind for opening the Inspect panel. 
For Windows, its Ctrl + Shift + I.