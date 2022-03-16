---
layout: project
type: project
image: images/puregym_scraper_sq.png
title: What's the best time to go to the gym?
permalink: projects/puregym_scraper
# All dates must be YYYY-MM-DD format!
date: 2019-12-18
labels:
  - Python
  - Raspberry Pi
  - Web scraping
  - Spline interpolation
summary: I investigated the best time to go to the gym, by scraping the current number of people in the gym at 5-minute intervals over several weeks.
---

The number of people in the gym varies with time of day, and with day of the week. To investigate the best time to go to the gym, I wrote code to:

<ul>
  <li>Login to the gym website and scrape the number of people currently at the gym, at 5-minute intervals</li>
  <li>Process the scraped data: transforming to simply time of day and day of the week</li>
  <li>Use spline interpolation to fit a line of best fit for each day of the week</li>
  <li>Plot the scraped data, along with the lines of best fit</li>
</ul> 

I deployed the code for scraping to a Raspberry Pi, and let it run constantly for just over a month in late 2019.

This is the result:

<p style="text-align:center;"><img src="/images/puregym_scraper.png" alt="graph" style="max-width: 100%;"></p>

So, roughly speaking, the gym gets quieter with each passing day from Monday. There are strong peaks of people going to the gym before work, at lunch time, and immediately after work.


The code is available at [GitHub](https://github.com/jackgrimes/puregym-scraper).



