---
layout: post
title: Regression (Part II)
---
<p>OK, on with the show.  So after scraping away at movie websites like <a href="boxofficemojo.com"></a>, <a href="metacritic.com"></a>, I learned a valuable lesson:  web scraping without a real problem to solve, is like scraping ice off your car when there's no ice on it.  After contemplating topics focused on the Oscars and Studio success or critical acclaim, I decided to focus on something different all together:  sports movies.  The premise was this, despite recent successes of movies like "Creed" and "Concussion", the sports genre still remains an underdog in comparison with other more established genres.</p>
<p>Despite, what I had scraped, it wasn't focused on sports movies, so it was back to the drawing board.  After some searching, I found a website, <a href="http://www.ultimatemovierankings.com/Top-400-sports-movies/">Ultimate Moving Rankings</a>, that maintained a list of the Top 400 sports movies of all time.  The advantages of this source was that the data was concise and easy to scrape, it was categorized by sport, and its domestic gross numbers were adjusted for inflation.  Among the cons, the overall feature set ended up being limited and some of the features where aggregates that included values from other features, making them difficult to use as independent variables.  Nevertheless, there was enough to work with to start my regression analysis.</p>
<p>First I looked at the top movies by specific sport.  Not surprisingly, boxing, football, and baseball movies outplayed the rest of the field significantly.  The complete rankings are shown in the histogram below.</p>
<figure class="half">
    <a href="/images/top-sports-movies.png"><img src="/images/top-sports-movies.png"></a>
    <figcaption><center>Top Sports Genre Movies by Actual Sport</center></figcaption>
</figure>
<p>Next, I looked at the trends over time, which showed that despite the box office successes of the "Rocky" franchise and occasional blockbusters like "Jerry Maguire" and "The Blind Side", sports movies really aren't that popular.  In fact, the peak of their popularity was much early in the data set, during the 1940's and 1950's, when sports themselves weren't as accessible on television or in-person.</p>
</p>Finally, I conducted an actual linear regression using critical audience/rating as a predictor for adjusted domestic gross.  Despite a low R-squared value, due largely to the outliers (i.e. your Rocky's, and Blind Side's), there was a correlation between the two variables.  However, if you look at the slope of the regression graph, it is fairly gradual, affirming that despite critical acclaim, sports movies really don't move the meter that much.</p>
<figure class="half">
    <a href="/images/sports-regression.png"><img src="/images/sports-regression.png"></a>
    <figcaption><center>Adjusted Domestic Gross vs. Critical Acclaim</center></figcaption>
</figure>
<p>Given more time, I would have liked to explore additional features, and compare against similar data for other genres to see how bleek the outlook for sports movies really is.  Additionally, as mentioned earlier, gathering data on sports attendance and viewership would also be an interesting relationship to explore.  Go figure, in a time when sports are so ubiquitous in our society, sports movies are effectively down for the count.</p>
