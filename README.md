# CNRec
CNRec Dataset Associated with Content based News Recommendation via Shortest Entity Distance over Knowledge Graph

CNRec.zip should contain the following files:

wc *.???

   300    300  19704 articleToID.csv
 16201  16201 554493 CNRec_All_Data.csv
  5401   5401 165913 CNRec_groundTruth.csv
 21902  21902 740110 total

CNRec_groundTruth.csv contains the following fields:

art1	art2	meanGoodR	meanSimRating	GoodR_75	GoodR_50	pair_id	diversity_75	diversity_50

-art1: id of the first article in the pair
-art2: id of the second article in the pair
-meanGoodR: the mean good recommendation rating across the six participants 
-meanSimRating: the mean similarity rating across the six participants
-GoodR_75: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.75
-GoodR_50: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.5
-pair_id: the id of the pair of articles (note that the pair 1 0 and 0 1 share the same pair ID)
-diversity_75: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.75 and the meanSimRating was <= 1
-diversity_50: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.5 and the meanSimRating was <= 1

CNRec_All_Data has the following fields:

art1	art2	rating	goodR	username	time	rating_id	pair_id

art1: id of the first article in the pair
art2: id of the second article in the pair
rating: the similarity rating of 0/ 1 / 2
goodR: the good recommendation rating of 0 or 1
username: Which user made the rating, either A, B, C, D ,E, or F
time: the time at which the rating was made
pair_id: the id of the pair of articles

articleToID.csv consists of two fields:

art fileName

art: the article ID
filename: name of the article in the CNRec_RawText folder

The CNRec_RawText folder should contain 300 articles:

find CNRec_RawText/ -type f | wc -l
300




