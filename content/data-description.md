---
title: Community Analysis
prev: "/"
next: Community Analysis
---

As mentioned the full dataset did not make a fully connected graph, and instead many subnetworks appeared. The largest connected component consists of 21.627 products. This component helped understand what factors influence the purchasing patterns of pet supply customers. When computing community splits on the largest connected component, we can group the purchases, with items that they are often more bought with than others. This results in a split, that we can visualize, with each community of items bought together having different colors.

![](/images/largest_component.png)

We can see some really clear communities, with some being larger than others. To understand what the items in each community are, we can use the reviews to get an understanding.

Word clouds are produced that can fit to each community. In the word clouds we typically see one animal being very large, meaning it’s mentioned a lot, with a few other words also appearing large, that give good indication in what the items are. These are for example in group 0: Bird and cage, in group 1: Dog and brush. 

![](/images/word_cloud.png)

A way to further understand the items in each community was to look at the IDF of the words used to the reviews. Here we can see what is more unique for the groups, and what defines them, and we do not have non-important words like “use” taking over. These are shown in the [Explainer Notebook](explainer-notebook.html), for the 5 largest communities, to complete our understanding of the items within each group.
From the community analysis we found that people tend to buy multiple items, that are for the same animal, and are within the same category of item. So bird seeds are also bought with a bird feeder. This is the main factor that results in co-purchases, and something Amazon or potential buyers should notice to find their next recommendation.


