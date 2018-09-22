## Newspaper
In the shared Box folder, you can find the files containing the downloaded news articles and metadata under /presidency_project/newspaper/ny2/, /presidency_project/newspaper/wp/, and /presidency_project/newspaper/wsj/. You can find the most recently saved R objects under /presidency_project_/newspaper/workspaceR/

* Clean up `readNews.R`: Currently, when I update with another month of news, the code reads in all the months of news again anew. This takes longer than necessary. It should be re-written to load the previously saved RData file, read in only the newest articles and metadata and either (1) transform these, and add them to the tm corpus, and recreate the quanteda corpus completely, or (2) transform these and add them to the prior quanteda corpus (not sure if I need the tm corpus -- maybe, if we want to add additional cleaning steps via tm_map as problems are realized). Probably other bits could be better, too.

  * Aycan
* Run `exploreNews.R` and look for words, phrases that need to be normalized across the three newspapers. For instance, `readNews.R` already makes a few changes like changing F.B.I in the NYT to FBI to match the WSJ, or trying to change the appearance of U.S. in the WSJ to United States to match the NYT. But I suspect the current clean up isn't sufficient either because not everything worked and there are more phrases and abbreviations specific to a news source. We need another set of eyes to start capturing these so we can beef up and correct the reading/cleaning file.

  * Leah
* Create a new version of `complexityNews.R` using sentences as unit (e.g., `complexityNews_sent.R`: this should start with the same data object that `complexityNews.R` uses, but first reshape `qcorpus2` to sentences. It should create a new metadata data frame like `qmeta2` (e.g., `qmeta2_sent <- docvars(qcorpus2_sent`) and add the complexity/readability score to the dataframe.

  * Sofia

* Create version of `sentimentNews.R` using sentences as unit: as above, this should start with the saem data object that `sentimentNews.R` uses (ideally, it would start with the saved data object from `complexityNews_sent.R`, but that's not created yet -- we can sequence them later), but will need to reshape `qcorpus2` to sentences. And this, too, should create a new metadata frame like `qmeta2` and add the various sentiment scores to the dataframe.

  * Sofia

* To be added:* ran out of time; will include improvements to topic model script, working through issue rhetoric identification

  
## Additional Sources

* Look into possibility of scraping key internet news sites on right and left. First need to identify/justify what are key native digital news sites on right/left; e.g., Politico, Breitbart, or something else, selected by audience size/ideological center. May or may not be able to acquire from January 20, 2017 on, but could we at least set up something going forward?

## Cable News

* *To be added:* ran out of time; will include reviewing topictiling, validating initial results (e.g., against Vanderbilt News Archive's story count for Anderson Cooper, other ways?), figure out how to containerize the process (via singularity) to run on the cluster. 

## Tweets

* *To be added:* ran out of time

## Presidential Documents

* *To be added:* ran out of time

