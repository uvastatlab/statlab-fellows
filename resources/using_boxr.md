## Getting Started with `boxr`

`boxr` is an R package that allows you to work directly with files in your box.com account. Below are instructions for how to set it up and a quck example of what it can do.

These instructions were created in October 2018 for version 0.3.4 of `boxr`. They are different from what is currently provided in the vignette accompanying the package. 

## Setting up `boxr`. Only need to do one time.

1. Go to https://developer.box.com/
2. click Console button
3. Click create new app
4. Select Custom App, click Next
5. Select Standard OAuth 2.0 (User Authentication), click Next
6. Name your app, doesn’t matter what you name it. Not really an app. I did “DFD”. Click Create App
7. Click View Your App
8. Enter http://localhost as your Redirect URI
9. Click Save Changes
10. Go to R and run the following two lines of code

`library(boxr)`  
`box_auth()`

11. Enter your box client id and hit ENTER 
12. Enter your box client secret and hit ENTER

(Both client id and client secret are on the Configuration page of your App)
Web browser should open where you can grant yourself access to your files at box.com

## Example of using `boxr`

Instead of this....  

`setwd("~/Box Sync/mpc/dataForDemocracy/presidency_project/newspaper/")`   
`source("codeR/readFactivaHTML3.R")`

We can do this....   

`library(boxr)`   
`box_setwd(18051534353)`   
`box_source(283963253938)`   

The directory and file id numbers are visible in the URL. If you go to, say, the “newspaper” folder under “presidency_project”, the URL is https://virginia.app.box.com/folder/18051534353. 18051534353 is the id number for the newspaper directory. Likewise, clicking (or hovering over) the link for “readFactivaHTML3.R” reveals the id number 283963253938.
