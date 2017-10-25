# CNRec
CNRec Dataset Associated with Content based News Recommendation via Shortest Entity Distance over Knowledge Graph

CNRec.zip should contain the following files:

wc *.???

   300    300  19704 articleToID.csv <br />
 16201  16201 554493 CNRec_All_Data.csv <br />
  5401   5401 165913 CNRec_groundTruth.csv <br />
 21902  21902 740110 total <br />

### CNRec_groundTruth.csv 

Contains the following fields:

<li> art1: id of the first article in the pair <br />
<li> art2: id of the second article in the pair <br />
<li> meanGoodR: the mean good recommendation rating across the six participants <br />
<li> meanSimRating: the mean similarity rating across the six participants <br />
<li> GoodR_75: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.75 <br />
<li> GoodR_50: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.5 <br />
<li> pair_id: the id of the pair of articles (note that the pair 1 0 and 0 1 share the same pair ID) <br />
<li> diversity_75: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.75 and the meanSimRating was <= 1 <br />
<li> diversity_50: A indicator value of 0 or 1 if it should be considered a good recommendation if the meanGoodR was >= 0.5 and the meanSimRating was <= 1 <br />

### CNRec_All_Data 

Has the following fields:

<li> art1: id of the first article in the pair <br />
<li> art2: id of the second article in the pair <br />
<li> rating: the similarity rating of 0/ 1 / 2 <br />
<li> goodR: the good recommendation rating of 0 or 1 <br />
<li> username: Which user made the rating, either A, B, C, D ,E, or F <br />
<li> time: the time at which the rating was made <br />
<li> pair_id: the id of the pair of articles <br />

### articleToID.csv 

Consists of two fields:

<li> art: the article ID <br />
<li> filename: name of the article in the CNRec_RawText folder <br />

### CNRec_RawText folder 

Should contain 300 articles:

find CNRec_RawText/ -type f | wc -l
300




