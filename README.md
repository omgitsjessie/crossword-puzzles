# wine-ratings

Using data from 2019, dig into some visualizations around the world of wine ratings.
Data Source: https://github.com/rfordatascience/tidytuesday/tree/master/data/2019/2019-05-28

# Data Dictionary
### `winemag-data-130k-v2.csv`

|variable              |class     |description |
|:---|:---|:-----------|
|country               |character | Country of origin |
|description           |character | Flavors and taste profile as written by reviewer |
|designation | character | The vineyard within the winery where the grapes that made the wine are from |
|points                |double    | The number of points WineEnthusiast rated the wine on a scale of 1-100 (though they say they only post reviews for wines that score >=80) |
|price                 |double    | The cost for a bottle of the wine |
|province              |character | The province or state that the wine is from|
|region_1              |character | The wine growing area in a province or state (ie Napa) |
|taster_name           |character | The taster/reviewer |
|title                 |character | The title of the wine review, which often contains the vintage (year) |
|variety               |character | Grape type |
|winery                |character | The winery that made the wine |


## What words are more likely to be used to describe to specific wine varieties?

Here we can use tidylo to look at the probabilities that individual words are used in a particular variety (Merlot, Chardonnay, etc), compared to the how often that word is used OUTSIDE of that variety. This gives us a list of language used to describe different wine types -- perfect if, like me, you have no idea what you're doing with wine other than enjoying it.  Fake your way through any fancy party with this easy trick:

![](images/wine_variety_words.png)

## Do people describe higher-scoring wines the same way they describe lower-scoring ones

Looking at some simple scatterplots, we can look at how description length changes relative to the wine point score. Here, it looks like higher-scoring wines do tend to use more words! It looks like there's no real difference in the word length, so people generally aren't using more complex words for better-scoring wine. 

![](images/wine_descriptions_vs_points.png)
