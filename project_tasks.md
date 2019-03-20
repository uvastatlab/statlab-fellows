## Newspaper
In the shared Box folder, you can find the files containing the downloaded news articles and metadata under /presidency_project/newspaper/ny2/, /presidency_project/newspaper/wp/, and /presidency_project/newspaper/wsj/. You can find the most recently saved R objects under /presidency_project_/newspaper/workspaceR/


* Data cleaning -- probably still need to remove odd publication-specific phrases and strings from texts. The best place to do this is `exploreNews.R` -- potential ways of checking include the keyness metric (implemented in `exploreNews.R` or examination of words in topics from the topic model (e.g., results from `stmTopicModelNews.R`).

* Sentence-level analysis -- create parallel versions of `complexityNews.R`, `sentimentNews.R`, `moralFoundation1.R`, and `stmTopicModelNews.R` using sentences as the unit of analysis rather than articles. (e.g., `complexityNews_sent.R`: this should start with the same data object that `complexityNews.R` uses, but first reshape `qcorpus2` to sentences. It should create a new metadata data frame like `qmeta2` (e.g., `qmeta2_sent <- docvars(qcorpus2_sent`) and add the complexity/readability score to the dataframe.

* Try [Lexicoder Topic Dictionary](http://www.lexicoder.com/download.html) -- generate `policyNews.R` and `policyNews_sent.R` (beginning with output of `sentimentNews.R` and `sentimentNews_sent.R`) to implement policy/issue attention in articles using the Lexicoder Topic Dictionary. I think this can be implemented with the liwcalike function in the [quanteda.dictionaries package](https://rdrr.io/github/kbenoit/quanteda.dictionaries/man/liwcalike.html). Evaluation of results -- e.g., to sample articles/sentences scored highly on major topics appear to be correctly assigned?

* Generate `positionNews.R` and `positionNews_sent.R` to test ideological position of text using Wordfish ([see example here](http://quanteda.io/articles/pkgdown/examples/plotting.html)). I don't expect this to work very well, but evaluation of the results can provide some ideas about how to improve measures in this corpus, and ideological/policy positioning is a key feature in comparison of news treatment (particularly with regard to charges of bias).
  
  * Leah

* Test policy position of text using [Laver and Garry's WordStat dictionary](https://provalisresearch.com/products/content-analysis-software/wordstat-dictionary/laver-garry-dictionary-of-policy-position/), availale as part of the quanteda.dictionaries package. Again, I don't expect this to work very well -- having been developed for party platform-style texts using UK parties. Could a Laver-Garry style dictionary be built for this case (e.g., using party platforms to identify keywords)?

* Start named entity recognition process (might be better in Python?): in particular, extracting persons, organizations, and geographical or geopolitical entities is key. I'm less clear on how we want to store this -- it won't be as neatly structured as the other attributes extracted from the text so far. But in addition to including this in the larger feature data frame eventually, the entitites also lend themselves to other analytic approaches (e.g., networks). For some sources


  
## Additional Sources

* Look into possibility of scraping key internet news sites on right and left. First need to identify/justify what are key native digital news sites on right/left; e.g., Politico, Breitbart, or something else, selected by audience size/ideological center. May or may not be able to acquire from January 20, 2017 on, but could we at least set up something going forward?

## Cable News

* Trouble shooting the acquisition of the final two months of Anderson Cooper and Erin Burnett -- `acquire_cnn.R`

* Start reading in cable news transcripts (whole). This is likely to be more complicated than it sounds. Ultimately, we want to build a corpus of the transcripts, and some of the header info in the transcripts (which varies across shows) could be useful metadata.

* Further consideration of topictiling, initially whether the transcripts themselves have info that could help identify how many distinct segments are contained in the show; or possibly using Vanderbilt News Archive's story count for available shows (not many overlap).

* Further implementation of topictiling, figure out how to containerize the process (via singularity) to run on the cluster. And evaluation.

## Presidential Documents

* Trouble shooting the acquisition of the last few months of presidential documents (website changed so current script doesn't work; having trouble identifying elements). Only have through late October 2018.

* Generate series of scripts for presidential documents. To begin, need to separate `analyze_presdoc.R` into an exploratory script (the parts just looking at the text in multiple ways) and a feature extraction script (where features are being added to a document dataframe -- complexity, sentiment, policy/issues, topics, etc.) -- mirroring the features being extracted for newspapers.


## Tweets

* Generate series of scripts for tweets. To begin, need to separate `analyze_twitter.R` into an exploratory script (the parts just looking at the text in multiple ways) and a feature extraction script (where features are being added to a document dataframe -- complexity, sentiment, policy/issues, topics, etc.) -- mirroring the features being extracted for newspapers.

