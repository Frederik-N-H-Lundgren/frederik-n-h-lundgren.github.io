---
title: Graph Analysis
layout: single
next: data-description
---
This webpage is an overview of our findings of our project on co-purchases of pet supplies, on Amazon. We did this project because of the love for our dog, and the knowledge that every pet brings happiness. But it is not always easy to know which toys to buy, or snacks to stock up on. This is why we wanted to analyze the co-purchase patterns of Amazon pet supplies and answer if there is a relationship between the price of a pet supply product and the sentiment of its reviews, and if higher-priced products tend to receive higher ratings compared to lower-priced alternatives.
We also wanted to know which factors influence the purchasing patterns of pet supply customers, and how these factors affect the product review.

Some people might now want the full analysis, and just want to know which items are commonly bought for their type of pet. Up in the corner you can find pages more dedicated to looking at commonly co-bought items for specific animals, and some more light and funny analysis of the graph, as well as a community analysis.


![](/images/Arrow.png)

The data that comprises this project, is a combination of metadata for products in the Amazon put supply category, and the reviews for these products. All of this data has been gathered by McAuley Lab, and is available for download online.
The dataset gathered is large, which leads us to only look at pet supply products and nothing else, and only use reviews from 2017 and forward. To add on this, any product without a review, would not be included.

This left us being able to build a graph, based on the products and their co-purchases with 32.792 nodes (products) and having 211.455 edges, which produces a quite low density network. The pet supply network varies in degree, with the highest being 1.191 meaning it’s been bought with a lot of other items, and the lowest being 0 degree. This means it is not a fully connected graph, and we have a largest connected component, which appears later in the webpage. More basic graph analysis can be found in the helper notebook.

As you will see throughout this website we describe products with an id called “asin”. This was part of the metadata that was collected, and it’s the way Amazon describes the products. There is not a clear translation to find the product from this id, unless you are Amazon, but a few websites can convert some of the asin to the real products. But for all the research on the different pets and all the items in this analysis, the asin will be the products id. To identify the product of the asin you are referred to the metadata where you can locate the asin within the dataframe as well as more specifications such as price, categories and description.

When looking at the entire graph, we found something interesting between the highest degree nodes, being items that are often bought with other things, such as a natural dog treat with asin: B001HBBQKY, having the highest node degree, or a cat litter with the second highest degree, and some of the items with 0 degree. These 0 degree items are not bought with any other pet supply item, and consist mostly of dog clothing. 
The ratings given on amazon for these two widely different items in the graph, are really close, and this also goes for the sentiment score of the reviews given to the items. From this we can conclude that items that are typically bought with many other items, are not necessarily more beloved by the users than stand alone items.

In a wider look of all the items we can see a slight trend that higher rated products will also have better sentiment scores, which indicate more positive language in high rated products, even with the massive size of the data, that make the plot bizarre.

![](/images/rating_vs_sentiment.png)

Not everyone can spend a fortune on their pets items, which led us to look if you had to pay extra to get a more liked product. This was done by calculating the sentiment score of product reviews, and plotting this against the price of it.

![](/images/sentiment_vs_price.png)

As we can see there is nothing that shows spending more money results in items with better sentiment from their reviews. The same method was also used to compare price to the rating of the product, and again we do not see anything suggesting that you have to spend more money for more liked and well rated products, which could be a relief for many.




