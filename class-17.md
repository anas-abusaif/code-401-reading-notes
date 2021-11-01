# Web Scraping

Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort.

## Important notes about web scraping:

1. Read through the website’s Terms and Conditions to understand how you can legally use the data. Most sites prohibit you from using the data for commercial purposes.
2. Make sure you are not downloading data at too rapid a rate because this may break the website. You may potentially be blocked from the site as well.

The first thing that we need to do is to figure out where we can locate the links to the files we want to download inside the multiple levels of HTML tags. Simply put, there is a lot of code on a website page and we want to find the relevant pieces of code that contains our data.

If you click on the arrow on the top left at the inspect window and then click on an area of the site itself, the code for that particular item will be highlighted in the console. I’ve clicked on the very first data file, Saturday, September 22, 2018 and the console has highlighted in blue the link to that particular file.

Notice that all the .txt files are inside the `<a>` tag following the line above. As you do more web scraping, you will find that the `<a>` is used for hyperlinks.
Now that we’ve identified the location of the links, let’s get started on coding!

Python Code
We start by importing the following libraries.
```
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
```

Next, we set the url to the website and access the site with our requests library.
```
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```

Next we parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure. If you are interested in learning more about this library, check out the BeatifulSoup documentation.
```
soup = BeautifulSoup(response.text, “html.parser”)
```
We use the method .findAll to locate all of our `<a>` tags.
```
soup.findAll('a')
```