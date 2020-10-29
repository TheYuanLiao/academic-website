---
title: "Interactive explorer of origin-destination matrices: a Shiny app and how-to"
date: 2020-10-28
author: admin
image:
  placement: 3
  caption: 'Image credit: [**Alina Grubnyak**](https://unsplash.com/photos/ZiQkhI7417A)'
---

**Interactive ODM explorer** [^1]
Below is a Shiny app which you can interactively explore origin-destination (OD) matrices based on the [travel survey](https://doi.org/10.17026/dans-xxt-9d28) of the Netherlands (2017). It is featured with
- OD matrices broken down by mode (Non-bike, bike, and e-bike) and time (0 - 23)
- Interactive visualization of the networks
- Data come from North Holland which is known by its popularity of biking

{{< minipage "https://yuanliao.shinyapps.io/InteractiveODM/" >}}


## Data preparation
With travel surveys, the first thing to do is to convert travel survey trip records into origin-destination pairs with a zoning system.

{{< minipage "zones.html" >}}

A typical OD flow dataset looks like the below.


| Origin zone  | Destination zone | Trip number |
| ------------- | ------------- | ------------- |
| 100  | 100  | 45  |
| 101  | 100  | 78  |
| 100  | 101  | 22  |
| 101  | 114  | 1  |


And to make the zone id just like the zoning system, there is a great tutorial on how to generate OD polylines with the origin and destination of each connection consistent with their polygons' centroid.

> [Origin-destination data with stplanr](https://cran.r-project.org/web/packages/stplanr/vignettes/stplanr-od.html)

## A Shiny app



[^1]: I've been taking [Data Science Specialization](https://www.coursera.org/specializations/jhu-data-science) on Coursera. This post is based on the final project of Course 9/10 [Developing Data Products](https://www.coursera.org/learn/data-products).
