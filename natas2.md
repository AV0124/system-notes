# Natas2 | OverTheWire Natas Wargame

### Entering Credentials
- natas2
- TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI

### Challenge
Instead of finding the password of the next level commented inside the page  source as usual, we see something else. We have to dig deeper. Or maybe dig...upwards?

### Solution
As usual, we open the Inspect panel and check the Elements section. 

We see this sticking out:
~~~
<div id="content">
There is nothing on this page
<img src="files/pixel.png">
</div>
~~~

While the page claims there is nothing on it, there is actually something  hidden-- a pixel.png image in the files folder.
Just like the File Explorer in your PC, Webpages have a directory of their own which is used to store files. We can navigate to different sub-directories or folders within by entering in its the full address in the search box.
There are two types of addresses used: Absolute and Relative. The address of the pixel image is a Relative Address, as it starts from a 'files' folder. All w1e have to do is to append the Relative Address to our webpage's url, which would be http://natas2.natas.labs.overthewire.org/files/pixel.png to open the image file.

But the pixel.png is blank, and has almost no exploitable information attached to it. Cause its a red herring! The purpose of the file's existence was not the file itself, but to let us know there exists a 'files' sub-directory in the webpage which we can navigate to. Simply remove the 'pixel.png' from the url and press Enter.

NOW we see something really interesting. The index of 'files' reveals that there is a hidden text file with it. As we did for the pixel image file, all we have to do is to append the text file's name with the url.

Inside, we see a bunch of 'username:password' mappings.
One of the lines says: 'natas3:3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH'
That is it! The password of username natas3 is given alongside it.

## Takeaway: Webpages have their own directories and subdirectories which are hidden. These can be explored with their addresses.