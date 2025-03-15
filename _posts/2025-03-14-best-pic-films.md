---
layout: post
title:  "And the Oscar Goes To..."
description: "me, who spent countless of hours on this project. Just kidding! But seriously, what determines if a movie gets nominated and wins the Academy Award's Best Picture? Is it luck? Or is it calculated? Let's find out..."
image: /assets/img/oscars.jpg
---


## A Little Fun Fact

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/family.jpg)

I watched a lot of movies growing up with my parents. But not the fairytale princess movies. We're talking about every type of genre with basically every type of accent you could think of. The way for my parents to learn and understand English, was watching movies. My siblings and I would join and help translate along the way if they ever had any questions. By now, my parents are better at understanding a British accent than me...

But because I grew up watching so many movies, I became really curious about them. How are they made? What goes down behind the scenes? What does the writing process look like? Stuff like that. If you're a film fanatic, then you get it.

One of my never-ending questions is: what makes a film win the Best Picture award? Is there a specific trend? Or is it just pure opinion and luck? So in this blog post, we're going to dive deep into the question: What features (if any) contribute to a film winning the Academy Award for Best Picture?

#### The Features
There's A LOT that goes into making a movie. But for both of our sakes, we're only going to focus on a few. The most promidant ones that I thought we should look into are the following:

- Year the film was released (then separated into decades)
- The title (obviously huh?)
- Whether or not it won
- The IMDb rating
- Runtime (length of the film)
- Director(s)
- Leading Actors
- Writer(s)
- Distributor
- Prodcucer(s)
- Genre(s)
- Box office earnings (how much did the film make?)

Hopefully just by looking at these, we can figure out whether or not there's a pattern.



##### Data Collection
This is the part that I think every data scientist or analyst underestimates. It can't be THAT hard right? WRONG. Get ready to get your hands dirty during this process. 

Where was I going to get all the information about the films? If you're thinking IMDb, then you're just as wrong as I was... Turns out that IMDb is super protective about their films' information and because I didn't want to pay $10,000 to get data, I had to look elsewhere. And I looked. And looked. And looked.

Turns out that the only site that had a list of all the nominees and winners for Best Picture was the OG Wikipedia. Using this <a href="https://en.wikipedia.org/wiki/Academy_Award_for_Best_Picture" target="_blank">Academy Award for Best Picture</a> page, I was able to get the year, title, distributor, producers, and whether it won or not. 

Still missing some data, a friend of mine recommended using an API from <a href="http://www.omdbapi.com" target="_blank">The Open Movie Database</a>. This had most of the information I needed such as, the genres, IMDb rating, runtime, directors, actors, writers, and box office earnings (missing for most old films). The OMDb API has much more information if you're curious and want to check it out.



###### Tag, You're It
You can do this too by using BeautifulSoup on Python. Using the HTML parser, you can webscrape the year and title right off of the table in the Wikipedia page <a href="https://en.wikipedia.org/wiki/Academy_Award_for_Best_Picture" target="_blank">(link)</a>. Finding out whether it won or not is trickier, you want to find a way where it identifies when the title is highlighted (winner) versus when it's not (nominee). For the distributor and producers, you'll have to webscrape the Wikipedia link to the film and go through there to identify the distributors and producers for each film.

For the OMDb API, you'll have to request a key (super easy). Again, using BeautifulSoup and your API key, pass through all the films' titles and years released. The API should output the necessary information - you just need to extract it.



##### Data Cleaning
I wish I could say that cleaning the data was all fun and rainbows, but it was super tedious.
First off, the OMDb API won't have the necessary information for older films so I excluded the years 1927-1933. You don't have to exclude them, but I did because it's neater. 

From the list of distributors and producers that you've scraped from Wikipedia, you'll want to clean them. Make sure all the names are separate but within their respective movie row. Remove any numbers or brackets. Separate the years into bins to see their respective decades.

With the information gathered from the API, remove the "min" from the runtimes and the "$" from box office. Double check that the following factors are the following types:
- Year (integer)
- Decade (category)
- Winner (boolean)
- IMDb Rating and Box Office (float)
- Runtime (integer or float)
- Movie, Director, actors, writers, distributors, producers, genres (string)

Convert if necessary. Create a dataframe with all of them. Should look like the following:

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/dataframehead.png)

##### Several Fun Facts

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/didyouknow.jpg)

After gathering all the data I needed, I wanted to share some quick highlights that I learned! Some are basic information, others are more interesting! I hope you learn something just as much as me.


Number of observations (films): 575
Winners: 91
Nominees: 484


Who directed the most films by decade?
- 1930s: Frank-Capra (5)
- 1940s: Sam Wood (5)
- 1950s: George Stevens (4)
- 1960s: Stanley Kramer (3)
- 1970s: Francis Ford Coppola (4)
- 1980s: Steven Spielberg (3)
- 1990s: Frank Darabont (2)
- 2000s: Clint Eastwood (3)
- 2010s: Steven Spielberg (4)
- 2020s: Denis Villenueve (2)

Top 10 genres among Best Picture winners:
1. Drama (82)
2. Romance (22)
3. Biography (20)
4. Comedy (19)
5. Crime (12)
6. Adventure, War, & History (10)
7. Musical (7)
8. Family & Thriller (6)
9. Music (4)
10. Mystery, Action, & Sport (3)

Top Best Picture Directors (nominated/winners):
1. William Wyler (13)
2. Steven Spielberg (13)
3. Martin Scorsese (10)
4. George Stevens & John Ford (7)
5. Fred Zinnemann, Sam Wood, Victor Fleming, Mervyn LeRoy, George Cukor, Michael Curtiz, & Frank Capra (6)

Top Actors among Best Picture winners:
1. Clark Gable (3)
2. Morgan Freeman (3)
3. Jack Nicholson (3)
4. Dustin Hoffman (3)

Top Actors among Best Picture nominees:
1. Leonardo DiCaprio (9)
2. Robert De Niro (9)
3. Tom Hanks (9)
4. William Holden (8)

Top Distributors for Best Picture winners:
1. Columbia Pictures (12)
2. United Artists (11)
3. Paramount Pictures (10)
4. Warner Bros. Pictures (8)
5. Universal Pictures (6)

Distributions for IMDb Ratings & Runtime:
![Figure]({{site.url}}/{{site.baseurl}}/assets/img/ratings.jpg)

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/runtime.jpg)



There are a lot more highlights but for the sake of this post, those are the ones I found most interesting!


##### Summary
This is the part when the beautiful cookies finally come out of the oven and we get to decorate them! After the analysis is finished, we have to present our findings. This is where we can create graphs, charts, and plots to make our data visually appealing for viewers. We could use different platforms to do so such as <a href="https://www.tableau.com/why-tableau/what-is-tableau" target="_blank">Tableau</a>, <a href="https://matplotlib.org" target="_blank">Matplotlib</a>, and <a href="https://seaborn.pydata.org" target="_blank">Seaborn</a>.

The type of presentation you want to use will depend on your type of data. We could use line graphs, histograms, box plots, scatter plots, bar charts, etc:

###### Line Graph
![Figure]({{site.url}}/{{site.baseurl}}/assets/img/linegraph.png)

###### Histogram
![Figure]({{site.url}}/{{site.baseurl}}/assets/img/histogram.jpg)

###### Box Plot
![Figure]({{site.url}}/{{site.baseurl}}/assets/img/boxplot.jpg)

###### Scatter Plot
![Figure]({{site.url}}/{{site.baseurl}}/assets/img/scatterplot.png)

###### Bar Chart
![Figure]({{site.url}}/{{site.baseurl}}/assets/img/barchart.png)

Then we present our product!


##### 5. Decision-Making
Now that we have all of our cookies, we tasted them, we can make a conclusion on which flavors we like best. We can say whether chocolate-chip-oatmeal cookies are a nice combo or if white-chocolate-peanut-butter is a tasty combo or not. We can share with our family and friends how we came up with the combination and how enjoyable (or not) the process was.

In other words, after we have a nice graph, chart, or plot, we can tell a story and make predictions. We can use the insights that we've gained during this process to guide our decision-making process. Let's look at an example!

This following link will take you to a page of the United States Census Bureau website. Go ahead and clink on this <a href="https://www.census.gov/library/visualizations/interactive/assets-and-debts.html" target="_blank">link</a>

I'll wait...

This specific page has a line graph over time of net worth, assets, and debt of households from the years 2017-2022. Click on the dark blue tab at the top that says "Net Worth" then click on the dropdown arrow where it says "Select chart." As you can see there's multipe options available, go ahead and click "Education." You should see a nice line graph that looks like this:

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/networth.jpg)


This is a graph that somebody already made. They collected data from the census, cleaned it, analyzed it, then made this nice graph. Now if we were them, we could tell a nice story and make a prediction of whether or not the level of education completed correlates (influences) with the net worth of a household. 

If I were the storyteller here, I would say that the higher the level of education completed, the higher the net worth of a household. Then I could make a decision of whether or not I wanted to pursue a graduate degree or not. Based off of the information the graph provides, I would pursue a graduate degree, knowing that my household's net worth would also increase.

#### Wrap-up
Okay ladies and gents, that was a quick overview of data science! Younger me would be so proud to explain to her Mexican parents what data science is. It's the collection, cleaning, manipulation, and presentation of data. Just like baking cookies. 

If you felt comfortable with the explanation in this post, go ahead and check out IBM's page about data science <a href="https://www.ibm.com/think/topics/data-science" target="_blank">here</a>! Keep learning and expanding. If you know anyone who is also curious to know what data science is, share this post with them! If they don't want to read it because they think they'll get confused, let them know it's Data Science for Dummies.




