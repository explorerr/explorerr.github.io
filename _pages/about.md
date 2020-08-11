---
permalink: /
title: "Happy Exploring"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
Dr. Zhang is a Research Scientist at the IBM T.J. Watson Research Center, where she works in the AI department, more specifically in the area of physical science and analytics. She works on the core of an IBM product called [PAIRS](https://www.ibm.com/us-en/marketplace/geospatial-big-data-analytics) -- Physical Analytics Integrated data Repository and Services.

Her expertise lies in Deep Learning in remote sensing data, time series analysis/forecast, big data platform for spatial and temporal data, and distribubted training for large scale Deep Learning models. In her PhD, she did advanced large scale adaptive meshing algorithms for Computation Fluid Dynamics simulations, and energy simulation for buildings.


Selected projects:
---------------


Map Generation from Large Scale Incomplete and Inaccurate Labels 
---------------
[Paper](https://arxiv.org/pdf/1703.10593.pdf) | [Presentation](https://youtu.be/RXxh1PMvLW0) | [Short Promotional Video](https://youtu.be/6pZJmnIUTAc)

<iframe width="560" height="315" src="https://www.youtube.com/embed/6pZJmnIUTAc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


-Example Open Street Map Labels:
-![Example OSM labels](/images/osm_sample.png "Example OSM labels") 


-Example of generated maps:
-![Example of generated maps](/images/front.png "Edxample of generated maps")


-Publicly available label data for map generation from high resolution remote sensing imageries are not accurate nor complete. We have proposed and implemented an modeling approach with incremental data augmentation which can generate maps as accurately as the models trained on accurate data labels. 
-Exploiting the fact that CycleGan does not require paired images, which shows better generalization power, we have been able to use a variant of cycleGan to augment the training data with more accurate labels, and yielding a better trained U-Net model for the map generation task 

-Since scaling the mapping task to CONUS, we applied an Decentralized Parallel Stochastic Gradient Descent (DP-SGD) training scheme that is scalable to hundreds of GPUs with near linear speed-up. We demonstrated an implementation of the DP-SGD scheme and achieved a speed up of 14.7 times over a cluster of 16 GPUs.

<!---
-Unlike previous studies, most of which use datasets that are available only in a few cities across the world, we utilizes publicly available imagery and map data, both of which cover the contiguous United States (CONUS).
-We approach the technical challenge of inaccurate and incomplete training data adopting state-of-the-art convolutional neural network architectures such as the U-Net and the CycleGAN to incrementally generate maps with increasingly more accurate and more complete labels of man-made infrastructure such as roads and houses.
Results show that we achieved a recall-score of 84.9%, and precision score of 95% in a subset using manual count in terms of house detection in selected four cities in Texas. 

-->

Spark Solution for PAIRS Batch Export and Overview Layer Generation 
---------------

Exploiting the Z-Order index spatio-temporal data stored in HBase, a spark solution is optimized with minimum shuffle operations to perform batch exports and spatial aggregations.
-![Spark](/images/combined.png "Spark")

-
-Batch Exports
  -Batch query on spatio-temporal indexed HBase DataBase with Petabytes of data.
  -Fast query speed with optimized solution that minimize shuffle operation in Spark.
  -Exporting Terabytes in minutes.
  -Supporting Deep Learning training data generation.

-
-Saptial Aggregation:
  -Overview Layers are spatial aggregated layer.
  -Overview layers are used for data exploration at different level of spatial resolutions.
  

Solar Forecasting
---------------

- nnnn

-

Leak Detection for High Pressure Gap Pipeline
---------------

- nnnn

-


-Conformal 3D Mesh Generation for Free Style Architectural Design
---------------

- nnnn

-

-Adaptive 2D Mesh Generation Architecture Designs
---------------


- nnnn

-
