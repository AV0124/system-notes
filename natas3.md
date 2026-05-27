# Natas3 | OverTheWire Natas Wargame

### Entering Credentials
- natas3
- 3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH

### Challenge
In the Elements section, we view the page source and realize there is a comment gloating about how there are no more information leaks. Not even GOOGLE can find it.

### Solution
Google is the key! It always is. But in particular Googlebot is the key.

Google acquires the information it uses to give search results by using 'crawler' or scraper bots that go through the internet, scraping information. Google uses an ethical, obedient crawler bot that can be instructed on what pages of a website it is allowed to scrape data from, and which ones it must leave alone.
Other search engines like Bing also use scraper bots that follow instructions like that.  They are often called Web Bots.

These instructions are put in a text file called 'robots.txt' which are placed within a website's home directory.

In the text file, there is a 'User Agent' term which is essentially what web bot must follow the given instructions. A '*' includes all web bots.
The 'Disallow' term tells the web bots what pages they must not scrape from, which can be pages holding sensitive information. This is done by giving the address of the directory or sub-directory which should be excluded from scraping.

The text file can be accessed be appending 'robots.txt' to the url of the webpage.

In it we can see this:
~~~
User-agent: *
Disallow: /s3cr3t/
~~~

The robots.txt file, if not used correctly, can reveal the address of other pages or directories, just like how we found the address of '/s3cr3t/'.
Opening the new webpage, we see a file 'users.txt' within it. Following the pattern of the previous level, the password is given here for natas4.


## Takeaway: Irresponsible or incorrect use of robots.txt can leak the addresses of important webpages.