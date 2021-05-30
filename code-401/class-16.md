# Web Scraping

Web scraping is a technique to automatically access and extract large amounts of information from a website.

Web spiders should ideally follow the robot.txt file for a website while scraping. It has specific rules for good behavior such as how frequently you can scrape, which pages allow scraping, and which ones you can’t.

You can find the robot.txt file on websites. It is usually the root directory of a website – `http://example.com/robots.txt.`

Here are a few easy giveaways that you are bot/scraper/crawler –

- scraping too fast and too many pages, faster than a human ever can
- following the same pattern while crawling.
- too many requests from the same IP address in a very short time
- not identifying as a popular browser. You can do this by specifying a ‘User-Agent’.
- using a user agent string of a very old browser

A user agent is a tool that tells the server which web browser is being used. If the user agent is not set, websites won’t let you view content. Every request made from a web browser contains a user-agent header and using the same user-agent consistently leads to the detection of a bot.

How can websites detect and block web scraping?

1. Unusual traffic/high download rate
2. Repetitive tasks performed on the website in the same browsing pattern
3. Checking if you are real browser
4. Detection through honeypots 
> honeypots are usually links which aren’t visible to a normal user but only to a spider. When a scraper/spider tries to access the link, the alarms are tripped.
