## Microsoft Studio Project

### Repository Contents
- Overview
- Business Problem
- Data Understanding and Analysis
  - Source of data
  - Description of data
  - Visualizations 
- Conclusion
- Summary of conclusions including three relevant findings

### Overview
Microsoft is creating a new movie studio. As it prepares to create original video content, it seeks to understand the film industry. We, the advisory team, explored movie production data to help Microsoft successfully launch its first film. We started by conducting a web scrape to extract two datasets containing all the relevant film information. We then merged our datasets and cleaned our data by turning certain strings into integers, adjusting dates to show more details, removing Null values, and adding a column for the rate of return based on the production budget and box office returns. Once the data was clean, we created plots to determine which genres had the highest rate of return, which release dates yielded the highest revenue by genre, and which runtimes were optimal for each genre. Based on the data, we determined that horror films yielded the highest rate of return. The best month to release a horror film is October, and the most optimal film length is 90-105 minutes.

### Data Understanding & Analysis
The available datasets included data from The Numbers and IMDb, online databases containing movie industry information. The Numbers data included variables necessary for our analysis, such as production budget and gross profits, while the IMDb data included other important variables, like genres. However, merging these datasets resulted in a significant loss of movies to analyze resulting from numerous unmatched values. Due to this loss, the advisory team acquired additional data by scraping The Numbers website. The complete chart (https://www.the-numbers.com/movie/budgets/all) consisted of all films in their database that includes financial information.

The dataset contains a total of 6,100 films ranging over almost a hundred years, including films release this year, which is larger and more recent than the data set we initially had. It also contains the variables from the other data sets that we initially targeted. Therefore, the advisory team decided to use this data set for our analysis.

We merged our two datasets together, creating a data set with the following variables:

- Budget and gross figures to be used in finding profits and losses
- Genres to be compared with one another
- Release date to be sliced into day, month, and quarter of the years
- Runtime in minutes to compare longer and shorter films

Given the domestic gross and worldwide gross, we used the worldwide box office returns to analyze the correlation between production budget and overall profits. The resulting correlation was not strong enough to make a definitive conclusion aout the data. We decide to zoom in on how each genre performed instead.

![profits_vs_budget (1)](https://user-images.githubusercontent.com/79488205/145619111-0854a99e-dc7b-4f0b-94d4-31e481c0723d.png)

We compared the profit ratio and production costs and found that horror films yield the highest rate of return, resulting in a return of 3:1 profits versus production costs, compared to the 2:1 profit versus production cost ratio resulting from action and adventure movies. 

![profits_per_genre (1)](https://user-images.githubusercontent.com/79488205/145619504-73caccde-482e-4c03-9bd4-54a436e6f389.png)

After discovering that horror films yielded the highest return on investment, we took a look at the horror movies' performance and found that the popularity of horror films have increased over the past 40 forty years, making this an attractive genre on which to focus Microsoft’s resources. This analysis prompted us to explore the horror movies more closely to determine if there were discernible trends within this profitable genre.

![horror_count_years (1)](https://user-images.githubusercontent.com/79488205/145619564-a8446c33-f6e0-4234-a384-96f2621f7582.png)

![horror_count_profit (2)](https://user-images.githubusercontent.com/79488205/145619588-a2dd417f-a9b2-4465-b394-a07ce0aeffdc.png)

We looked at release dates to see if there was a certain time of year that was best to release horror movies. After separating profitable horror movies from unprofitable horror movies, we saw that October was the most popular month by count for profitable horror films to be released. September was the most popular month by count for unprofitable horror films to be released.

![horror_per_month (1)](https://user-images.githubusercontent.com/79488205/145619629-53b787e8-1913-4c15-aab2-d6a15e448319.png)

Going further, we also examined the runtime of profitable and unprofitable movies to see if there was a relationship to profitability. We chose to look at median runtimes in order to reduce the effect of outliers on our analysis. The median runtime of profitable movies is 107 minutes; for unprofitable movies, the median runtime is 103. This 4-minute difference doesn’t really tell us a lot, so we examined runtime by genre. We found that different genres have different median runtimes, with horror having a median runtime of 96 minutes. Calculating the interquartile range gives us a runtime of 90-105 minutes, which is a reasonable window for Microsoft to aim for their movies’ runtimes.

![movie_runtime (1)](https://user-images.githubusercontent.com/79488205/145619777-786681d3-a4e1-4a16-ac41-520c7200a139.png)
![runtime_per_genre](https://user-images.githubusercontent.com/79488205/145619690-7d79d98d-3c63-42b0-ae6d-051538f2f648.png)

Based on the findings from our data analysis, we recommend that Microsoft focus on producing films within the horror genre, as horror movies have the highest rate of return of any genre. Moreover, horror movies are increasing in popularity over the past 40 years, as evidenced by the number of releases by year.

The most profitable month to release horror films is, perhaps unsurprisingly, in October. Of special note, our analysis revealed the least profitable month for horror films is September, so we urge Microsoft not to release a horror film until October begins. The median runtime for horror movies is 96 minutes, with the bulk spanning 90-105 minutes. We therefore recommend that Microsoft release horror films in October with a runtime between 90-105 minutes.

We do caution that this may not be a guarantee for success at Microsoft’s movie studio. For one, since Microsoft is just beginning to make films, it does not yet have an established reputation. This may make people wary of going to see their films initially. Additionally, movie quality is important. If the movies have uninspired plots, poor acting, and sloppy edits, they may not prove to be profitable.

For that reason, one future course of inquiry would be to analyze the impact of specific directors and actors on a movie’s profitability. Utilizing well-known and respected movie talent would likely increase people’s confidence in the film’s quality and give it a greater chance of ending up as a quality product.

Another mode of inquiry would be to determine what the most critically acclaimed films are. Those with the highest reviews or most awards may not be the most profitable, but perhaps Microsoft wants to focus on establishing a reputation for quality films, especially as it builds its movie catalog. Proving its ability to make interesting and creative movies would likely attract popular and skilled film industry talent, thereby further increasing the quality of Microsoft’s movies and resulting in greater profitability.

### Repository Structure
```

├── data
|   ├── tngross.csv
|   ├── tnproduction.csv

├── data_cleaning
│   ├── check_for_duplicates.csv
│   ├── czarina_release_date_analysis.ipynb
│   └── olgert_earnings_vs_budget.ipynb
│   ├── sally_runtime_correlations.ipynb
│   └── valeria_genre_vs_profits.ipynb

├── data_scraping
│   ├── Scrape Numbers.ipynb
│   ├── Scrape links.ipynb


├── images
│   ├── horror_count_profit.png
│   ├── horror_count_years.png
│   ├── horror_pe

```
