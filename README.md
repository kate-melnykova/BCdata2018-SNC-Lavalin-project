# BCdata2018-SNC-Lavalin-project
BCdata workshop for SNC-Lavalin data
**Hosted by:** SNC-Lavalin  
**Mentor:** Cameron Wallace  
**Project Room:** ORCH 3072
**Official website for workshop:** http://workshop.bcdata.ca/2018/ 
**More detailed (working) repository** https://github.com/slemonide/workshop-content18/tree/master/3-snc/src
![Sample ship path](https://github.com/kate-melnykova/BCdata2018-SNC-Lavalin-project/blob/main/snc-lavalin-sample-ship-path.png)
## Summary

As part of a study for the Port Authority of Vancouver, cargo ship positions
reported by their navigation systems were considered. These discrete positions
were pieced together into full ship routes which were then used to estimate the
amount and distribution of pollution generated by cargo traffic through the port
of Vancouver. In the original study, there was difficulty handling missing or
erroneous position data. This project is to improve the reconstruction process
of ship routes. Specifically, the problem is to look through the data to find
all the records for a particular ship over a ten day period, and:

1. generate a route map for the ship over that ten day period;
2. identify when there is bad data for the ship and correct it so that the
  resulting route map is as close as possible to what it should be;
3. for bonus marks, make sure the routes don’t go over land (find open data to
  describe the coastline in polygons, and incorporate it).

Alternatively, identify characteristics that might flag “good” data vs. “bad”
data (i.e. speed variations), and identify ways to systematically correct for
bad data without minimum variation of the route. Identify the number of trips
that would be caught and fixed with the methods.

Please visit the
[project page](http://workshop.bcdata.ca/2018/project/project-3/) for a full
description of the problem.

## INTERPOLATING SHIP PATHS

In the PIMS BC Data Science Workshop, we aim to approximate the ship path from the measurement. The simplest model (interpolation of the path from consecutive measurements) does not provide the accuracy needed as it does not consider the noise and time between measurements (missing or noisy measurements). During this workshop, we developed a method based on the Kalman filter to resolve these issues. The model shows good performance both on current data with dense measurements and old data with sparser measurements. The next stage of the project is to cluster the paths in order to apply the knowledge gathered from densely sampled paths to sparsely sampled paths. This brings new challenges like defining a good metric for paths and number of clusters, which is still ongoing.



## About 

Founded in 1911, [SNC-Lavalin](http://www.snclavalin.com/en/) is a global fully integrated professional services and project management company and a major player in the ownership of infrastructure. Our teams provide solutions in capital investment, consulting, design, engineering, construction, sustaining capital and operations and maintenance in many fields.

## Resources

Information on AIS data (and more AIS data!) is availble at the links below. In
particular, the Wikipedia contains a section describing the column names of the
data.

* [Wikipedia](https://www.wikiwand.com/en/Automatic_identification_system#/Detailed_description:_Class_A_units)
  for a description of the columns in the data.
* [aishub](http://www.aishub.net/stations): it's possible they have *more* data
  if necessary.
* [marinetraffic](https://www.marinetraffic.com/en/p/ais-historical-data): it's
  possible they have historical AIS data available - especially and including
  [for research](https://www.marinetraffic.com/en/p/ais-for-research).
