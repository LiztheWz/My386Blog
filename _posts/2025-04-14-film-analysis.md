---
layout: post
description: "Let's roll out the red carpet for some good old EDA (Exploratory Data Analysis) on Best Picture winners!"
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

Directors are the visionaries of film-making; they provide the artistic vision. So of course, we have to explore into which directors get nominated and win the most. The way we can do this is to calculate the proportion of wins for each director. In other words, divide the number of films that won Best Picture by the total number of films they were nominated for. 

However, we run into a messy problem. Let's say that someone directs a movie for the first time and somehow by extreme luck, they win Best Picture. Their proportion for wins would be 100%. Not very helpful, right? So we filter for directors that have AT LEAST 5 nominated films. This way we can calculate a more realistic proportion.

The following graph shows the top ten directors for highest proportion of wins. Note, some of these directors are deceased, but still appear due to their proportion of wins.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/director_proportion.png)

We can see that 40% of the time, Directors Billy Wilder's (who is deceased), Clint Eastwood's, and Francis Ford Coppola's films win the Academy Award for Best Picture. Of course, there's a lot of other talented directors not displayed! Take Steven Spielberg for example, who has a total of 13 nominations but not that many wins - hence the lower proportion compared to other directors.


#### Writers
Being able to write a compelling film is a huge task to undertake. The plot captivates the audience and influences the voters a lot. Same as with the directors, I calculated for the proportion of wins for writers with at least five nominated films.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/writer_proportion.png)

Francis Ford Coppola takes the lead with half the films he has written winning Best Picture. Following him is Billy Wilder at 29%, and Ethan Coen, Joel Coen, Steven Zaillian, and William Shakespear at 20%.

#### Producers
Producers, unlike the directors, deal with the practical execution of the film. Hence, all the logistical planning, hiring, and financial management falls under their roof. The process of film-making is no joke so these guys have a pretty big responsibility under their belt.

Again, the same process of calculating for proportion was done.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/producer_proportion.png)

First place goes to Arnon Milchan, with 40% of films winning. Second place goes to Brad Pitt (surprising for me too). Then we got, David O. Selznick and Jeremy Kleiner at 25%.

#### Distributors
The last feature we'll be focusing for the sake of this post's length (I don't want to keep you reading for too long) are the distributors. The only key difference between this feature and the others is that distributors are companies rather than people. I was a little puzzled with how to explore this feature, so I calculated the number of film nominees and winners produced under each company.

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/distributor_counts.png)

Looking at the graph initially, I assumed that Paramount Picture would take the lead when it came to winners. However, when I calculated the proportion. This was the result:

![Figure]({{site.url}}/{{site.baseurl}}/assets/img/distributor_proportion.png)

Turns out, Orion Pictures took first place at a whopping 57%!



