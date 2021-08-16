# Web Scraping

## [What is Web Scraping?](https://en.wikipedia.org/wiki/Web_scraping)

Web scraping typically extracts large amounts of data from websites for a variety of uses such as price monitoring, enriching machine learning models, financial data aggregation, monitoring consumer sentiment, news tracking, etc. Browsers show data from a website. However, manually copy data from multiple sources for retrieval in a central place can be very tedious and time-consuming. Web scraping tools essentially automate this manual process.

#### What is Web Scraping or Data Mining?
Basics of Web Scraping
“Web scraping,” also called crawling or spidering, is the automated gathering of data from an online source usually from a website. While scraping is a great way to get massive amounts of data in relatively short timeframes, it does add stress to the server where the source hosted.


Web scraping typically extracts large amounts of data from websites for a variety of uses such as price monitoring, enriching machine learning models, financial data aggregation, monitoring consumer sentiment, news tracking, etc. Browsers show data from a website.

![web scraping](https://www.hirinfotech.com/wp-content/uploads/2019/10/What-is-Web-Scraping-1024x512.png)

#### Typical applications of web scraping
1- Social media sentiment analysis
2- E-Commerce pricing
3- Investment opportunities
4- Machine learning

### The 10 Best Web Scraping Tools


[Scraper API](https://www.scraperapi.com/)

[ScrapeSimple](https://www.scrapesimple.com/)

[Octoparse](https://www.octoparse.com/)

[ParseHub](https://www.parsehub.com/)

[Scrapy](https://scrapy.org)

[Diffbot](https://www.diffbot.com)

[Cheerio](https://cheerio.js.org)

[Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/)

[Puppeteer](https://github.com/GoogleChrome/puppeteer)

[Mozenda](https://www.mozenda.com/)


## [How to scrape websites without getting blocked](https://www.scrapehero.com/how-to-prevent-getting-blacklisted-while-scraping/)

#### Respect Robots.txt

Web spiders should ideally follow the robot.txt file for a website while scraping. It has specific rules for good behavior such as how frequently you can scrape, which pages allow scraping, and which ones you can’t. Some websites allow Google to scrape their websites, by not allowing any other websites to scrape.

+ You can find the robot.txt file on websites. It is usually the root directory of a website – http://example.com/robots.txt.

+ If it contains lines like the ones shown below, it means the site doesn’t like and does not want to be scraped.
`
User-agent: *

Disallow:/ 
`
#### Here are a few easy giveaways that you are bot/scraper/crawler –

+ scraping too fast and too many pages, faster than a human ever can following the same pattern while crawling. 

+ For example – go through all pages of search results, and go to each result only after grabbing links to them. No human ever does that.

+ too many requests from the same IP address in a very short time

+ not identifying as a popular browser. You can do this by specifying a ‘User-Agent’.

+ using a user agent string of a very old browser

#### There are several methods can be used to change your outgoing IP.

+ TOR
+ VPNs
+ Free Proxies
+ Shared Proxies – the least expensive proxies, shared by many users. Chances to get blocked are high.
+ Private Proxies – usually used only by you, and lower chances of getting blocked if you keep the frequency low.
+ Data Center Proxies, if you need a large number of IP Address and faster proxies, larger pools of IPs. They are cheaper than residential proxies and coulde be detected easily.
+ Residential Proxies, if you are making a huge number of requests to websites that block to actively. These are very expensive (and could be slower, as they are  real devices). Try everything else before getting a residential proxy.

**Most browsers sends more headers to the websites than just the User-Agent. For example, here is a set of headers a browser sent to Scrapeme.live (Our Web Scraping Test Site). It would be ideal to send these common request headers too.**

### The most basic ones are:

+ User-Agent
+ Accept
+ Accept-Language
+ Referer
+ DNT
+ Updgrade-Insecure-Requests
+ Cache-Control

#### Bot detection tools look for any flags that can tell them that the browser is being controlled through an automation library.

+ Presence of bot specific signatures
+ Support for nonstandard browser features
+ Presence of common automation tools such as Selenium, Puppeteer, Playwright, etc.
+ Human-generated events such as randomized Mouse Movement, Clicks, Scrolls, Tab Changes etc.



## [Web Scrape with Python in 4 minutes](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)
