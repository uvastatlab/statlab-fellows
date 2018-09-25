## 2018-09-25
* Consultations: 
    * Master of Science Student, Systems and Information Engineering; help with statistical analysis of experimental data. Had run 10 t-tests after an ANOVA. Suggested using adjusted p-values via Tukey’s pairwise comparisons. Also review how to check ANOVA assumptions.
    * undergraduate; help installing VMware client for the Hive, and then getting started with Stata on the hive.
    * EnviSci faculty; has dataset of atmospheric concentrations of numerous gases taken over time and space. Interested in analyzing the different contributions from different emission sources to the total concentrations. For example 50% of the methane concentration is attributed to oil/gas and 50% to rice cultivation. Very challenging consultation, especially since she doesn’t have any training data where she knows the proportion of contributions. 
    * Curry PhD candidate; seeking advice regarding how to handle missing data for mixed-effect modeling
    * UVa staff; provided some assistance with estimating power of a randomized complete block design for a given number of blocks.

* Research/Learning: 
    * Data Wrangling with R, part 2 and part 3 workshops
    * Review/Revise ggplot workshop

* Admin:
    * Town Hall meeting
    * R users meetup


## 2018-09-19
* Consultations: 
    * Commerce faculty; meeting to review and revise off-grounds housing web-scraping script to make it more robust to various departures from expected text. Made significant revisions to script.
    * Nursing PhD candidate; help merging date and time columns and formatting as date-time class. 
    * Staff, Emergency Medicine Research Office (EMRO); Trying to use the document-term matrix for association/cluster analysis. Suggested looking into topic-modeling at first but then realized cluster analysis might be better for what he wanted. Pointed to him some resources to help get him started. 
    * Grad student, Civil Engineering; Research involves using two types of neural networks to forecast groundwater level. Wanted to select better model. Suggested that instead of a t-test of the RMSEs between the two models that he take the difference in the 1000 RMSEs from the two models and analyze the distribution of differences with percentile/BCa intervals.
    * Undergrad, A&S; Needed some help understanding Excel instructions in a class assignment. Confused about how to use Excel to take a random sample from a sample frame.
* Research/Learning: 
    * final preparations for DWR part 3 workshop
    * Getting familiar with ggplot2 version 3 and seeing if there's anything of note to incorporate into my upcoming workshop
* StatLab article ideas (just some ideas off the top of my head! No guarantees!):
    * A primer/intro on using Stata's margin commands (possibly a series of articles)
    * A primer/intro on replicating the results of Stata's margin commands in R (possibly a series of articles)
    * Getting started with rate models
    * Getting started with CFA
    * Boostrapping basics with examples
    * Tips and strategies for simulating data in R


## 2018-09-10
* Admin:
    * Backed up Intro to R workshop. Always interesting to see what confuses new R users. This time someone was confusing objects in her global environment with files in her working directory. Totally understandable if you think about it.
* Consultations:
    * McIntire faculty; asked for help scraping housing information from the UVa off-Grounds Housing Service web site. Wrote an R script to do this: https://gist.github.com/clayford/3ddaca6b4d4f3d2daf8d9a49c8fbc5a2
* Research/Learning:
    * Getting ready for 3 part data wrangling with R workshop series.


## 2018-08-31
* Admin: fork statlab-fellows and sync public presidency repos; work with MPC to establish GitHub flow
* Consultations: 
    * Darden PhD candidate; help selecting, implementing and interpreting statistical analyses for his dissertation. 
    * Econ PhD; had some survey data she collected and noticed that a particular response seemed to depend on who asked the question. Suggested she run a mixed-effect model to control for the variation between survey administrators.
    * surgery resident; has data on vascular surgeries, wants to investigate whether or not certain medications are helpful post-surgery. Data is in Excel, has imported to Stata, wants help cleaning data in Stata. Data is restricted and requires access to a server. He could not access server or even get on Internet while in Brown. (I’ve noticed this a lot with medical employees.) Referred him to Data@HSL.
* Research/Learning:
    * non-linear regression
    * neural networks
    * simulating data from binary logistic model
    * Gelman, Honesty and Transparency are not enough: http://www.stat.columbia.edu/~gelman/research/published/ChanceEthics14.pdf
    * Gelman blog post, Some clues that this study has big big problems:
https://andrewgelman.com/2018/08/29/some-clues-that-this-study-had-big-big-problems/

