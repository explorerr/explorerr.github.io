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

Her expertise lies in the area of Deep Learning on remote sensing data, time series analysis/forecast, big data platform for spatial and temporal data, and distribubted training for large scale Deep Learning models. In her PhD, she did advanced large scale adaptive meshing algorithms for Computation Fluid Dynamics simulations, and energy simulation for buildings.


## Selected projects
----------------


### Map Generation from Large Scale Incomplete and Inaccurate Labels 
---------------
[Paper](https://arxiv.org/pdf/1703.10593.pdf) | [Presentation](https://youtu.be/RXxh1PMvLW0) | [Short Promotional Video](https://youtu.be/6pZJmnIUTAc)

<iframe width="560" height="315" src="https://www.youtube.com/embed/6pZJmnIUTAc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


Example of Open Street Map (OSM) labels
![Example OSM labels](/images/osm_sample.png "Example OSM labels") 

Example of generated maps
![Example of generated maps](/images/front.png "Edxample of generated maps")


+ Publicly available label data for map generation from high resolution remote sensing imageries are not accurate nor complete. We have proposed and implemented an modeling approach with incremental data augmentation which can generate maps as accurately as the models trained on accurate data labels. 
+ Exploiting the fact that CycleGan does not require paired images, which shows better generalization power, we have been able to use a variant of cycleGan to augment the training data with more accurate labels, and yielding a better trained U-Net model for the map generation task 

+ Since scaling the mapping task to CONUS, we applied an Decentralized Parallel Stochastic Gradient Descent (DP-SGD) training scheme that is scalable to hundreds of GPUs with near linear speed-up. We demonstrated an implementation of the DP-SGD scheme and achieved a speed up of 14.7 times over a cluster of 16 GPUs.

<!---
-Unlike previous studies, most of which use datasets that are available only in a few cities across the world, we utilizes publicly available imagery and map data, both of which cover the contiguous United States (CONUS).
-We approach the technical challenge of inaccurate and incomplete training data adopting state-of-the-art convolutional neural network architectures such as the U-Net and the CycleGAN to incrementally generate maps with increasingly more accurate and more complete labels of man-made infrastructure such as roads and houses.
Results show that we achieved a recall-score of 84.9%, and precision score of 95% in a subset using manual count in terms of house detection in selected four cities in Texas. 

-->

### Spark Solution for PAIRS Batch Export and Overview Layer Generation 
---------------

Exploiting the Z-Order index spatio-temporal data stored in HBase, a spark solution is optimized with minimum shuffle operations to perform batch exports and spatial aggregations.
![Spark](/images/combined.png "Spark")


#### Batch Exports
---------------

+ Batch query on spatio-temporal indexed HBase DataBase with Petabytes of data.
+ Fast query speed with optimized solution that minimize shuffle operation in Spark.
+ Exporting Terabytes in minutes.
+ Supporting Deep Learning training data generation.



#### Spatial Aggregation
---------------

+ Overview Layers are spatial aggregated layer.
+ Overview layers are used for data exploration at different level of spatial resolutions.
  

### Solar Forecasting
---------------
[Paper](https://ieeexplore.ieee.org/document/8588777)
![Solar](/images/solar_projects.png "Solar")

#### Forecast of Solar Production Using DCNN
+ Several deep convolutional neural networks utilizing high resolution weather forecast data exploring various temporal and spatial connectivities to capture the cloud movement pattern and its effect on forecasting solar energy generation for solar farms.
+ Comparing with state-of-the-art forecast error rate, we have been able to reduce the error rate from about 21% in the persistent model, to 15.1% from the SVR model, and to 11.8% from the convolutional neural networks. 


#### Rasterized Probabilistic Solar Forecast Using Near Real Time Geo-Stationary Satellite (GOES) Imageries
+ Using Deep Convolution Neural Network on near real time geo-stationary satellite (GOES) tmageries to first forecast future GOES images. 
    + image sequence to image sequence generation.
+ Then a gridded (rasterized) forecast of solar irradiance quantiles. 


### Leak Detection for High Pressure Gap Pipeline
---------------
[Paper](https://www.semanticscholar.org/paper/Preventive-Leak-Detection-for-High-Pressure-Gas-Zhang-Huang/dec3944c75c0c23e6f30c958d5efd5e58aecd376) 

![leak_detection](/images/leak_detection.png "leak_detection")

Two innovative and effective leak detection models: the big leak detection model that identiﬁes medium size leaks preceding big rupture events, and the small leak detection model that identiﬁes small leaks lasting for extended periods of time. The data mining was developed using unsupervised tasks analyzing billions of data records to identify leaks of different sizes and impacts, with very low false positive rates and early preventative detections.


### Conformal 3D Mesh Generation for Free Style Architectural Design
---------------
[Paper](https://www.researchgate.net/publication/228118810_Conformal_adaptive_hexahedral-dominant_mesh_generation_for_CFD_simulation_in_architectural_design_applications) | [Presentation](https://youtu.be/DhGdQhYkTlA) | [Git](https://github.com/explorerr/ot14)
<iframe width="560" height="315" src="https://www.youtube.com/embed/DhGdQhYkTlA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

![3d_mesh](/images/3d_mesh.png "3d_mesh")

Mesh generation is a critical and probably the most manually intensive step in CFD simulations in the architectural domain. One essential feature is the large span of dimensional scales that is encountered in design, particularly if the model aims to simulate indoor and outdoor conditions concurrently, e.g., site at the magnitude of kilometers while building elements at the magnitude of centimeters. In addressing the challenge this paper presents an approach to generate adaptive hexahedral-dominate meshes for CFD simulations in sustainable architectural design applications. Uniform all-hexahedral meshes and adaptive hexahedral-dominant meshes are both generated for natural ventilation simulation of a proposed retroﬁt building in Philadelphia. Simulation results show that adaptive hexahedral-dominate meshes generate very similar results of air change rate in the space due to natural ventilation, compared to all-hexahedral meshes yet with up to 90% reduction in number of elements in the domain, hence improve computation efﬁciency.

### Adaptive 2D Mesh Generation Architecture Designs
---------------
[Paper](https://www.sciencedirect.com/science/article/abs/pii/S0360132310001149)

![2d_mesh](/images/2d_mesh.png "2d_mesh")

A prototype meshing tool is developed to construct adaptive quadrilateral meshes from two-dimensional image data, e.g., architecture drawings. First the quadtree based isocontouring method is utilized to generate initial uniform quadrilateral meshes in the immediate region of the objects. Meshes are further decomposed into finer quads adaptively near the surface of the object without introducing any hanging nodes. Boundary layers are then generated using the pillowing technique and the thickness of the boundary layer is controlled to achieve the desired yþ values for different near wall turbulence models. Finally, meshes are extended to the ambient domain with desired sizes, where flow fields are assumed to be relatively steady. The developed tool has been employed to generate meshes for CFD simulations of scenarios commonly existing in the indoor and outdoor environment.
