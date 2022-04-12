# Web Scrape with Python
## overview
Web Scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort.

[More about web scraping](https://en.wikipedia.org/wiki/Web_scraping)

## inspecting the website
We need to do is to figure out where we can locate the links to the files we want to download inside the multiple levels of HTML tags.

- The location of the links should be like in the following example:
```
<a href=”data/nyct/turnstile/turnstile_180922.txt”>Saturday, September 22, 2018</a>
```

## Python Code

- import the following libraries.
```
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
[Build A Python App That Tracks Amazon Prices!](https://www.youtube.com/watch?v=Bg9r_yLk7VY&ab_channel=DevEd)
```

- Set the url to the website and access the site with our requests library.
```
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```

- Parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure.
```
soup = BeautifulSoup(response.text, “html.parser”)
```

- We use the method .findAll to locate all of our <a> tags
```
soup.findAll('a')
```
  
This code gives us every line of code that has an <a> tag. 
  
 -  extract the actual link that we want. Let’s test out the first link.
```
  one_a_tag = soup.findAll(‘a’)[38]
link = one_a_tag[‘href’]
```

  
should look like this:
  ```
  
# Import libraries
import requests
import urllib.request
import time
from bs4 import BeautifulSoup

# Set the URL you want to webscrape from
url = 'http://web.mta.info/developers/turnstile.html'

# Connect to the URL
response = requests.get(url)

# Parse HTML and save to BeautifulSoup object¶
soup = BeautifulSoup(response.text, "html.parser")

# To download the whole data set, let's do a for loop through all a tags
line_count = 1 #variable to track what line you are on
for one_a_tag in soup.findAll('a'):  #'a' tags are for links
    if line_count >= 36: #code for text files starts at line 36
        link = one_a_tag['href']
        download_url = 'http://web.mta.info/developers/'+ link
        urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:]) 
        time.sleep(1) #pause the code for a sec
    #add 1 for next line
    line_count +=1
  
  ```
  
[More](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)
  
  
## How to Scrape Websites Without Getting Blocked
  
### Respect Robots.txt
  
Web spiders should ideally follow the robot.txt file for a website while scraping. It has specific rules for good behavior, such as how frequently you can scrape, which pages allow scraping, and which ones you can’t.
  
If these are in the link, it means the website does'nt want to scrape.
- User-agent: *

- Disallow:/
  
  
Methods that could help scraping robots.txt files
 - Make the crawling slower, do not slam the server, treat websites nicely
 - Do not follow the same crawling pattern
 - Make requests through Proxies and rotate them as needed
  
  
[More](https://www.scrapehero.com/how-to-prevent-getting-blacklisted-while-scraping/)
  
