---
layout: post
description: "Let's roll out the red carpet for some good old EDA on Best Picture winners!"
title:  "Lights, Camera, Analysis!"
image: /assets/img/oscar-picture.jpg
---

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/cliffhanger.jpg)

## Recap
Hi, there! Welcome back to Part 2! Sorry to have let you in a cliffhanger... but I'm glad you made it back! So let's do a quick recap from last time. Last post, I explained a little bit about my film curiosities and wanted to determine what features (if any) contribute to a film winning the Academy Award for Best Picture. We talked a little bit about my cleaning struggles (I'm not a data Cinderella after all). Then we found some basic summaries about directors, genres, actors, distributors, etc. 

However, we never dove deep to find out if there truly is a correlation or relationships between a film's features and whether they won or not. So in this post, I'll be rolling out the red carpet to some interesting features that won more than others. 

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/genre.jpg)

#### Genres
Genre is a feature that is so vague and has so many possibilities. For example, a film could be a combination of drama, war, AND adventure. Because there are so many possibilities for a film, I had to separate each genre individually. After that, I was able to get a general idea of each genre's popularity.

The following graph shows the number of films that fall under each genre and whether it is a nominee (didn't win) or if it won the award for Best Picture.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/genre_counts.png)

As we can see from the graph (and from the previous post), drama is the genre that has the most wins. It is followed by romance, comedy, and biography. Therefore, it seems that the Academy of Motion Pictures Arts and Sciences (<a href="https://www.oscars.org/oscars/voting" target="_blank">AMPAS</a>) prefers those genres over others such as fantasy, horror, or sci-fi.


#### Directors

Directors are the visionaries of film-making; they provide the artistic vision. So of course, we have to explore into which directors get nominated and win the most. The way we can do this is to calculate the proportion of wins for each director.

However, we run into a messy problem. Let's say that someone directs a movie for the first time and somehow by extreme luck, they win Best Picture. Their proportion for wins would be 100%. Not very helpful, right? So we filter for directors that have AT LEAST 5 nominated films. This way we can calculate a more realistic proportion.

The following graph shows the top ten directors for highest proportion of wins.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/director_proportion.png)

We can see that 40% of the time, Directors Billy Wilder's (who is deceased), Clint Eastwood's, and Francis Ford Coppola's films win the Academy Award for Best Picture. Of course, there's a lot of other talented directors not displayed! Take Steven Spielberg for example, who has a total of 13 nominations but not that many wins - hence the lower proportion compared to other directors.


#### Writers
Being able to write a compelling film is a huge task to undertake. The plot captivates the audience and influences the voters a lot. Same as with the directors, I calculated for the proportion of wins for writers with at least five nominated films.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/writer_proportion.png)

Francis Ford Coppola takes the lead with half the films he has written winning Best Picture.

#### Producers
Producers, unlike the directors, deal with the practical execution of the film. Hence, all the logistical planning, hiring, and financial management falls under their roof. The process of film-making is no joke so these guys have a pretty big responsibility under their belt.

Again, the same process of calculating for proportion was done.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/producer_proportion.png)

First place goes to Arnon Milchan, with 40% of films winning. Second place goes to Brad Pitt (surprising for me too).

#### Distributors
The last feature we'll be focusing for the sake of this post's length (I don't want to keep you reading for too long) are the distributors. The only key difference between this feature and the others is that distributors are companies rather than people. I was a little puzzled with how to explore this feature, so I calculated the number of film nominees and winners produced under each company.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/distributor_counts.png)

Looking at the graph initially, I assumed that Paramount Picture would take the lead when it came to winners. However, when I calculated the win proportion. This was the result:

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/distributor_proportion.png)

Turns out, Orion Pictures took first place at a whopping 57%!

#### Streamlit App
Now, this is only but a small portion of the EDA that went down behind the scenes. It's super fun for the writer (me) to explain everything because I've seen it all. However, it's less fun for the reader (you) because you can only read about it. But I want you to see everything for yourself!

Meet my fellow data science friend, (<a href="https://blog.streamlit.io/streamlit-101-python-data-app/" target="_blank">Streamlit</a>). Streamlit is essentially an app online that allows you to see and explore data that data scientists and analysts have been exploring all along. 

If you click the following link, it should take you to the app I created specifically for this data: Liz's Awesome Oscars App.

You'll be able to discover the following:
- Top genres over the years
- Discover the films that each director made
- See the top genres actors have acted in
- Discover which films take the win for highest grossing in the decade

This is only but a few of the things you'll be able to do in the app. You'll see that in the app, you'll be able to explore some line graphs, histograms, tables, and bar charts of the data. You'll be able to input or select the specific variables you want to explore as well. For example, you can type in a name in the Director or Actor tab (they have to at least gotten nominated for Best Picture to be displayed) to see all the films they participated in. You can also select a specific distributor in the Distributor tab to see their bar charts. I'll let you play around with it for a while so you too can share my excitement about film data.

#### And the Conclusion Goes To...
A lot of features go into film-making. And after all this exploration, there's a lot we can learn from them. I don't work in Hollywood, however if I had to create THE perfect film to win the Academy Award for Best Picture next year, it would include the following:

- Runtime: 120 minutes (2 hours)
- Genres: Drama & Romance
- Director: Francis Ford Coppola
- Writer: Francis Ford Coppola
- Producer: Arnon Milchan
- Distributor: Orion Pictures
- Actors: Morgan Freeman, Russell Crowe, & Dustin Hoffman

Ideally, it would achieve:
- IMDb Rating: at least an 8.0
- Box Office: around $100,000,000

I don't support gambling, but if you were to place your bets in - I would look away. 

I hope you've had as much fun as me in this data journey! My invitation to you would be to share what you've learned about the Oscars with family and friends! Show them the Streamlit and have them explore as well. 

Feel free to look at my EDA code:
Github: https://github.com/LiztheWz/filmcode
