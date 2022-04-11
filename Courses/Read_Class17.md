# Web Scrape with Python
## overview
Web Scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort.

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

  
  
  
