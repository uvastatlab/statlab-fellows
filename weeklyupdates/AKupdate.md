11/14 
* Prepared sentimentNews_R to include lexicode dictionary 
1) There are differences between bing and lexicode - will present the differences in general tone between the two 
2) Ask about graphs - the current graphs are not very explanatory of changing sentiment - the sentiment doesn't fluctuate much 
3) Opeds might be a better place to look for sentiment 
4) Should we do text preparation - trimming, removing of stop words? 
5) Will try lexicode by removing negations 
6) # Need to output the text of each article in the corpus to separate file in common folder (e.g., writeCorpus from tm) - what does this mean? 
7) Will try to find an alternative way to compare sample document most positive and negative tones from bing and lexicode 

* Will push newsRead_R later today

10/30 

* Was going to push the R file, but I realized box stopped working for me - is trying to solve this issue
* Conducted a consulting session on my own last week 
* Read about sentiment analysis - continue working on the code 
* Working on multiple imputation  - code was working before, not anymore 

10/10 

* Completed the R file - it has boxr integration to uvabox/presidencyproject/newspaper folder. If ran currently, it will create quanteda files for the folders nyt, wp, wsj (ones that have already been created). But during this process, the code will also create nytnew, wpnew, wsjnew folders. If we would like to give the code a try, we should download news articles from these newspapers through August 1 to September 30, 2018 in nytnew, wpnew and wsjnew folders to double check that it works. Final product is saved in newspapercomp.Rdata in workspaceR


10/02

* Working on the R file 
* Completed a workshop on Git

09/25

* Learning multiple imputation to prepare for the blog post (I'm doing multiple imputation currently for a paper so I thought I'd start writing the blog in the meanwhile)
* Learning git branching / commits 
* Started working on the R code for my task - will look at it closer during the rest of the week

09/14 
 Ideas for blog: 
Python - 
1) if/else statements, for and while loops
2) Writing functions
3) Introduction to Parallel Computing 
4) Scraping Lexis-Nexis with Selenium
5) Introduction to Machine Learning - KNN, Decision Trees, Random Forest 
 R - 
1) Getting started with Multilevel Modeling - lme4 package 
2) Introduction to lattice graphs 
3) Multiple Imputation to deal with Missing Data 
4) sqldf package - merging datasets with date ranges 

09/18 

Task: 

I have started working on the first task, clean up readnews.R - what I'm thinking about doing is, depending on how we download new html from Lexis-Nexis, to put the newly downloaded files into a new folder and make DirSource() read only from that folder. Once those files are turned into corpus, delete the files in the new folder.
