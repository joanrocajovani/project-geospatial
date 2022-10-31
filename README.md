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

![country_game](https://user-images.githubusercontent.com/114917673/199007936-6d416881-0945-4ed7-b79a-91ee6e08dd30.JPG)
![country_design](https://user-images.githubusercontent.com/114917673/199007940-ed2076e9-6e85-4bcc-9c26-d1023173e3cf.JPG)
![country_funded](https://user-images.githubusercontent.com/114917673/199007944-98342730-ce95-4641-83f7-445dd040c329.JPG)


USA was first in all categories, UK was second and Canada 3rd in 2 categories. So I picked those..

### Choosing the cities

From there I wanted to pick one city for each of the countries. Since the US had much more companies than any other country, I analyzed the US cities separatedly.

NY and San Francisco were 1st and 2nd in all 3 categories but I chose NY because the city had more design companies. For the rest of the countries I chose London, which was first in all categories, and Toronto, which was the Canadian city with most companies in 2 out of 3 categories.

Next, I joined the 3 tables for each city and plotted all the companies on a map. Then, I chose a location that satisfied the 3 requisites at best.

**New York:**

![NY map](https://user-images.githubusercontent.com/114917673/199011040-cfca8719-3531-44ce-a8e1-6aedae36b921.JPG)

**Toronto:**

![Torontomap](https://user-images.githubusercontent.com/114917673/199011500-3777c380-0453-43cb-a764-b44f8626a580.JPG)

**London:**

![Londonmap](https://user-images.githubusercontent.com/114917673/199011643-8bd0c02f-295f-4240-8072-2a0dc71b2fd6.JPG)


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

![final table](https://user-images.githubusercontent.com/114917673/199011790-103b7830-dd36-4292-b2c2-9ed5cd28b2d4.JPG)

Finally, NY has the best score, and it also is the city with most design, gaming and financed companies. So the location of the company would be NYC.

