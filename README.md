# Project Geospatial:
### Author: Joan Roca Jovani

## Introduction
We were given the task to find the most optimal place to place a videogame company given some requisites:
- Designers like to go to design talks and share knowledge. There must be some nearby companies that also do design.
- 30% of the company staff have at least 1 child.
- Developers like to be near successful tech startups that have raised at least 1 Million dollars.
- Executives like Starbucks A LOT. Ensure there's a starbucks not too far.
- Account managers need to travel a lot.
Everyone in the company is between 25 and 40, give them some place to go party.
- The CEO is vegan.
- If you want to make the maintenance guy happy, a basketball stadium must be around 10 Km.
- The office dog—"Dobby" needs a hairdresser every month. Ensure there's one not too far away.

### Choosing the first parameters

Given all these, I decided the three most important aspects were:
- **Close to gaming companies**.
- **Close to companies with funding**.
- **Close to design companies**.

  
### Choosing the countries

From the companies database I got 3 filtered tables with the previous requisites. Then, I wanted to find the countries with most of them.

<img src="images/country_game.jpg" width="100" height="250">
<img src="images/country_funded.jpg" width="100" height="250">
<img src="images/country_design.jpg" width="100" height="250">

USA was first in all categories, UK was second and Canada 3rd in 2 categories. So I picked those and then I also picked Spain being my own country and one of the fastest-growing tech hubs in southern Europe.

### Choosing the cities

From there I wanted to pick one city for each of the countries. Since the US had much more companies than any other country, I analyzed the US cities separatedly.

**Insert Table**

From the US I chose NY and from the rest of companies I chose Toronto, London and Barcelona.

Next, I joined the 3 tables for each city and plotted all the companies on a map. Then, I chose a location that satisfied the 3 requisites at best.

**New York:**


**Toronto:**

**London:**

**Barcelona**

Afterwards, using the Foursquare API I calculated the distances to all demanded venues except the dog hairdresser because being something that is not important on a day-to-day basis. The table that I got is the following.

**Insert Table**

Finally I gave the following wheights to the importance of the venue:
- Basketball Court: 5%
- Starbucks: 20%
- Vegan Restaurant: 15%
- Airport: 25%
- Nightclub: 15%
- School: 20%

And with the previous weights I created a score ranking the cities from best to worst.



