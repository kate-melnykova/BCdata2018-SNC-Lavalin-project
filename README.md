# BCdata2018-SNC-Lavalin-project
BCdata workshop for SNC-Lavalin data

# INTERPOLATING SHIP PATHS


The Port Metro Vancouver aims to reduce air emissions caused by ships, trucks, and equipment. In response to this request, SNC-Lavalin investigates, in particular, the emission patterns caused by using ship engines. This requires an extensive data frame including variables such as the current location, velocity and acceleration over time. This is useful when calculating the pollution and total emission of a ship as they can be computed partly from the velocity and acceleration of the vessel along the path. However, the location of ships are tracked irregularly and the data is corrupted and missing.


In the PIMS BC Data Science Workshop, we aim to approximate the ship path from the measurement. The simplest model (interpolation of the path from consecutive measurements) does not provide the accuracy needed as it does not consider the noise and time between measurements. During this workshop, we developed a method based on the Kalman filter to resolve these issues. The model shows good performance both on current data with dense measurements and old data with sparser measurements. The next stage of the project is to cluster the paths in order to apply the knowledge gathered from densely sampled paths to sparsely sampled paths. This brings new challenges like defining a good metric for paths and number of clusters, which is still ongoing.
