## Fetching Different Nodes from a Webpage Using CSS Selector
Let us learn this new concept with an example from [Pluralsight Machine Learning Skills](https://www.pluralsight.com/browse/machine-learning) webpage. When you visit this webpage, scroll down a bit and you will see **Top Machine Learning courses** as visible in the image below:

![Imgur](https://i.imgur.com/K23Zc4E.png)

Each course consists of the following entities:
1. Course's name
2. Author's name
3. Difficulty level
4. Duration

So let us scrape these four entity details using R. But before we jump into the code, understand what all information can be gathered from the DevTools. You can visit [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools) for a quick overview.

When you are comfortable in using DevTools, press `Ctrl+Shift+I` or right-click and select `Inspect Element`. Once the DevTools dialog box opens, you can again right-click on any of the element available in the image provided above. This will take you to a screen similar to this:

![Imgur](https://i.imgur.com/NoDGrqV.png)

In the above image, you can observe two red rectangles:
1. **The left red rectangle**: It depicts the CSS for course name
2. **The right red rectangle**: It depicts the CSS for all these four entities

Notice that in the code you need to put selector which is visible in the L.H.S. rectangle. There is a slight difference between both rectangle contents. The R.H.S has spaces and has no `div.` initially. So if you replace all the spaces with a period and prefix the selector with `div.`, you get the content which is present in your L.H.S and the one which is required in the code.

Now, let us code with these CSS selectors:


```r
library(rvest)

link <- "https://www.pluralsight.com/browse/machine-learning"

driver <- read_html(link)

# Course Title
titles <- html_nodes(driver, "div.course-item__title") %>% html_text()

# Removing first two titles which are added from the 
# Top Machine Learning Paths (a section just above Top Machine Learning courses)
titles <- titles[3:32]

# Course Authors
authors <- html_nodes(driver, "div.course--item__list.course-item__author") %>% html_text()

# Course Level
level <- html_nodes(driver, "div.course--item__list.course-item__level") %>% html_text()

# Course Duration
duration <- html_nodes(driver, "div.course--item__list.course-item__duration") %>% html_text()

# Creating a final DataFrame
courses <- data.frame(titles, authors, level, duration)

# First 10 rows
# titles									authors			level		duration
# 1	Understanding Machine Learning						David Chappell		Beginner	43m
# 2	Understanding Machine Learning with R					Jerry Kurata		Beginner	1h 25m
# 3	Scalable Machine Learning with the Microsoft Machine Learning Server	Shawn Hainsworth	Advanced	2h 21m
# 4	Preparing Data for Machine Learning					Janani Ravi		Beginner	3h 24m
# 5	Understanding Machine Learning with Python				Jerry Kurata		Beginner	1h 54m
# 6	Production Machine Learning Systems					Google Cloud		Advanced	3h 18m
# 7	Machine Learning: Executive Briefing					Simon Allardice		Beginner	40m
# 8	Designing a Machine Learning Model					Janani Ravi		Intermediate	3h 25m
# 9	Machine Learning for Business Professionals				Google Cloud		Beginner	5h 24m
# 10	How Machine Learning Works						Paolo Perrotta		Beginner	2h 23m
```

Before you move on to the next section, notice that initially the image depicted only six courses and a **Show more** button. However, our method scraped all of the available courses which are even present inside the **Show more** button.  
