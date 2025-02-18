---
layout: post
title: "Data Science for Dummies"
description: "New to data science? Perfect! Ever wanted a basic, simple rundown of data science? You've come to the right place. So relax, no fancy mumbo jumbo words here. This will be super easy for you to understand. I promise."
image: /assets/img/chocolate_chip_cookie.jpg
---

## Intro to Data Science
### (for us simple minded folks)

I remember when I switched my major to data science and told my Mexican parents, they simply asked, "what is that?" And I had no idea how to respond. "I'm not quite sure, but I'm enjoying it." 

You would think I had enough knowledge to explain my own major, but apparently on the spot, I didn't. So what did I do? What any reasonable human being would also do. I googled it. But even Google seemed confusing at explaining what data science was. 

So this post is specifically made for those who are in the same boat as me a few years ago. What in the world is data science??

#### What is it? What does it include?
Let's start with the basics. In the most simple form, data science is the study and manipulation of, well, data. I like to think of the data science process like making cookies. You have to grab ingredients, mix them up, put it into the oven, and then you get a tasty batch of cookies afterwards to take to your friends. 

It's almost as if statistics, math, and computer science had a child and named it data science. Data science then gets some data, does some cool stuff with it that its parents taught it, and then presents it. It's kind of like all of us when we were kids coming home from school with a cool art project that we wanted to show our parents. 

In this post I'll be taking you through the instructions! Here's a quick overview of what to expect in the data science process:
1. Data Collection
2. Data Cleaning
3. Exploratory Data Analysis
4. Data Visualization
5. Decision-Making

This isn't really EVERYTHING, but it's the basics of what one should know. So by the end of this post, if someone asks "what is data science?" you should be able to respond with ease! Let's dive in...


##### 1. Data Collection 
In the cookie example, this is the part of the instructions that wants you to gather all your ingredients. Gather all the data you need! We can do this in several ways:

Direct collection - you go out and gather the data yourself. You can do this through surveys, experiments, observations, interviews, etc. This is anything that requires you to gather data first-hand. Or you could get pre-existing data that someone else already collected and has it all organized for you in a big table (dataset). A lot of websites nowadays have datasets ready for the taking. You would just need to webscrape it (take data from websites)!

##### 2. Data Cleaning
We want to double check to make sure none of our cookie ingredients have expired or have gotten bad. So double check on the eggs, butter, vanilla, etc. Just like a manufacturing company has a section that detects weird, abnormal products, we also need to detect any abnormal or "dirty" data in our datasets.

The way we do this is by handling missing values, outliers (data very extreme from others), removing duplicate values, and correcting inconsistencies. For example, let's say that a dataset has a column named "State." You have some rows that have "NY" and others that have "New York." They're the same thing but they're detected as different, so we have to fix inconsistencies like this, so they're all the same. If we have any missing values in the rows, we should probably get rid of those too (if appropriate).

No one would like to eat cookies made with rotten eggs right? Well, no one really wants to receive "dirty data" either. 

##### 3. Exploratory Data Analysis (EDA)
When you are making cookies, this is the mixing and baking part of the instructions. This is the part where statistics, math, and computer science meet. Here we manipulate data to identify trends, patterns, and make predictions.

In order to do so, we need tools. In data science there are so many programming languages we can use but the most efficient and popular ones are <a href="https://www.python.org" target="_blank">Python</a> (not the snake), <a href="https://www.r-project.org/about.html" target="_blank">R</a>, and <a href="https://www.codecademy.com/catalog/language/sql?g_network=g&g_productchannel=&g_adid=624951458056&g_locinterest=&g_keyword=sql%20for%20beginners&g_acctid=243-039-7011&g_adtype=&g_keywordid=kwd-1924370498&g_ifcreative=&g_campaign=account&g_locphysical=1026980&g_adgroupid=102526215778&g_productid=&g_source=%7Bsourceid%7D&g_merchantid=&g_placement=&g_partition=&g_campaignid=10030170703&g_ifproduct=&utm_id=t_kwd-1924370498:ag_102526215778:cp_10030170703:n_g:d_c&utm_source=google&utm_medium=paid-search&utm_term=sql%20for%20beginners&utm_campaign=US_Language:_Basic_-_Exact&utm_content=624951458056&g_adtype=search&g_acctid=243-039-7011&gad_source=1&gbraid=0AAAAAon8KZHZivikF_SZk0gftp9GP_Cqx&gclid=Cj0KCQiA_NC9BhCkARIsABSnSTb3B968wRvW9Z6UdfSlRGgbM8ijm-AsVRVGIhAlY2Qpjg_UdhtrktYaAiv8EALw_wcB" target="_blank">SQL</a> (pronounced sequel). When we are baking, we have different measuring cups; in data science, we have different programming languages that all have specific strengths.

This is the part of the data science process where we want to get insights. It's the "so what?" part. So yeah, we have all this data and information but it's not that useful until I get some kind of conclusion from it. All data is useless if you can't draw a conclusion. So we have to sort it, analyze it, then present it. During the EDA process it's good to ask yourself, "what do I want to know? What do I have to do to this dataset to find out?" 

##### 4. Data Visualization
This is the part when the beautiful cookies finally come out of the oven and we get to decorate them! After the analysis is finished, we have to present our findings. This is where we can create graphs, charts, and plots to make our data visually appealing for viewers. We could use different platforms to do so such as <a href="https://www.tableau.com/why-tableau/what-is-tableau" target="_blank">Tableau</a>, <a href="https://matplotlib.org" target="_blank">Matplotlib</a>, and <a href="https://seaborn.pydata.org" target="_blank">Seaborn</a>.

The type of presentation you want to use will depend on your type of data. We could use line graphs, histograms, box plots, scatter plots, bar charts, etc:

###### Line Graph

###### Histogram

###### Box Plot

###### Scatter Plot

###### Bar Chart


Then we present our product!


##### 5. Decision-Making
Now that we have all of our cookies, we tasted them, we can make a conclusion on which flavors we like best. We can say whether chocolate-chip-oatmeal cookies are a nice combo or if white-chocolate-peanut-butter is a tasty combo or not. We can share with our family and friends how we came up with the combination and how enjoyable (or not) the process was.

In other words, after we have a nice graph, chart, or plot, we can tell a story and make predictions. We can use the insights that we've gained during this process to guide our decision-making process. Let's look at an example!

This following link will take you to a page of the United States Census Bureau website. Go ahead and clink on this <a href="https://www.census.gov/library/visualizations/interactive/assets-and-debts.html" target="_blank">link</a>

I'll wait...

This specific page has a line graph over time of net worth, assets, and debt of households from the years 2017-2022. Click on the dark blue tab at the top that says "Net Worth" then click on the dropdown arrow where it says "Select chart." As you can see there's multipe options available, go ahead and click "Education." You should see a nice line graph that looks like this:

{% raw %}![Figure]({{site.url}}/{{site.baseurl}}/assets/img/networth.jpg){% endraw %}


This is a graph that somebody already made. They collected data from the census, cleaned it, analyzed it, then made this nice graph. Now if we were them, we could tell a nice story and make a prediction of whether or not the level of education completed correlates (influences) with the net worth of a household. 

If I were the storyteller here, I would say that the higher the level of education completed, the higher the net worth of a household. Then I could make a decision of whether or not I wanted to pursue a graduate degree or not. Based off of the information the graph provides, I would pursue a graduate degree, knowing that my household's net worth would also increase.

#### Wrap-up
Okay ladies and gents, that was a quick overview of data science! Younger me would be so proud to explain to her Mexican parents what data science is. It's the collection, cleaning, manipulation, and presentation of data. Just like baking cookies. 

If you felt comfortable with the explanation in this post, go ahead and check out IBM's page about data science <a href="https://www.ibm.com/think/topics/data-science" target="_blank">here</a>! Keep learning and expanding. If you know anyone who is also curious to know what data science is, share this post with them! If they don't want to read it because they think they'll get confused, let them know it's Data Science for Dummies.




