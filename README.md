# CNRec: Content News Recommendation Dataset
CNRec Dataset Associated with Content based News Recommendation via Shortest Entity Distance over Knowledge Graph

CNRec provides document to document similarity as well as whether a pair of articles was considered a good recommendation. The data set consists of 2700 pairs of news articles, selected from 30 groupings of 10 articles of human perceived similarity. In total we have 300 unique news articles originally published in a period of 3 consecutive days between August 25-28, 2014. Each article is paired with all other articles in the same group.  This results in 45 pairs that should produce positive similarity ratings. Another 45 pairs are randomly generated across other groups resulting in 2700 total pairs. The 3 day period, as well as the grouping and pairing procedure, provides a ideal set of articles to process. It allows engineers to focus on direct algorithm design rather than filtering relevant articles by time, or overlapping entities, before computations. 

## Annotation

Each pair of articles is rated by 6 human annotators against two questions:

1. In terms of content delivered, how similar do you think these two articles are? The annoators were given 3 choices: 
	* Not Similar
	* Similar
	* Very Similar
   
   Their answers were converted into numerical values 0/1/2.

2. If one of these articles was recommended based on the other would you have followed the link? Each annotator choose between: 
NO and YES, which were converted to numerical values 0/1.

## Dataset Files

CNRec.zip should contain the following files:

<li> articleToID.csv <br />
<li> CNRec_All_Data.csv <br />
<li> CNRec_groundTruth.csv <br />

and the following folder: CNRec_RawText

### CNRec_groundTruth

Contains the following fields:

* `art1`: id of the first article in the pair 
* `art2`: id of the second article in the pair 
* `meanGoodR`: the mean good recommendation rating across the six participants
* `meanSimRating`: the mean similarity rating across the six participants 
* `GoodR_75`: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.75
* `GoodR_50`: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.5
* `pair_id`: the id of the pair of articles (note that the pair 1 0 and 0 1 share the same pair ID) 
* `diversity_75`: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.75 and the meanSimRating was <= 1
* `diversity_50`: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.5 and the meanSimRating was <= 1 

### CNRec_All_Data 

Has the following fields:

* `art1`: id of the first article in the pair 
* `art2`: id of the second article in the pair 
* `rating`: the similarity rating of 0 / 1 / 2 
* `goodR`: the good recommendation rating of 0 or 1 
* `username`: Which user made the rating, either A, B, C, D ,E, or F
* `time`: the time at which the rating was made 
* `pair_id`: the id of the pair of articles 

### articleToID

Consists of two fields:

* `art`: the article ID 
* `filename`: name of the article in the CNRec_RawText folder

### CNRec_RawText folder 

Should contain 300 articles:

find CNRec_RawText/ -type f | wc -l
300




