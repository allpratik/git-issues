# GitHub Issue Stats Monitor

* GitHub Issue Stats monitor displays the issues of any github repository on basis of their reporting date.
* This solution is simple JS based webapp where we do following things:
  * User Submits the URL of the github repo 
  * We grab the specific paramters from the URL like ```username``` of the owner of repo and the ```repository name```.
  * Based on above paramters we query the GitHub API to fetch relevant issues.
  * Once the issues are received, we classify them on the basis of their ```creation_date```
  * Then we update our counter variables according to the date of creation of particular issue.
  
##Scope of Improvements 
1. The solution as now displays only first 30 records due to GitHub's pagination. So, to include all the open issues we can parse the link headers and include all the remaining issues.
2. We need to include local time zone support in order to decide between issue was opened today or yesterday. By default, system considers UTC zone. We can do it by using Moment.JS library to mitigate it.
3. We can build docker image of above solution and host it on Google's kubernetes.

###Further Scope of Improvements

1. We can include issue's label analysis (Simple Word Cloud, maybe) to exactly pin point that which service people are facinf more problem. If we plotted the same data against time-series, we might even pin point the changes, if any, which could be the probable reason for the issues. It can save tons of time of our support staff.
2. We can include analyze data the frequency of issues according to time, so that we can optimize the timings of support staff.


## Demo
[GitHub Issue's Stats](https://git-issue.herokuapp.com/)


