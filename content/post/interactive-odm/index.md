---
title: "Interactive explorer of origin-destination matrices: a Shiny app and how-to"
date: 2020-10-28
summary: "How to make a Shiny app that explores OD matrices by mode and time."

tags: ["R", "transport", "mode", "origin-destination matrix", "Shiny"]

image:
  caption: Photo by Alina Grubnyak on Unsplash
  focal_point: Smart
---

**Interactive ODM explorer** [^1]

Below is a Shiny app where you can interactively explore origin-destination (OD) matrices based on the [travel survey](https://doi.org/10.17026/dans-xxt-9d28) of the Netherlands (2017). It is featured with
- OD matrices broken down by mode (Non-bike, bike, and e-bike) and time (0 - 23)
- Interactive visualization of the networks
- Data come from North Holland which is known by its popularity of biking

{{< minipage "https://yuanliao.shinyapps.io/InteractiveODM/" >}}


## Data preparation
With travel surveys, the first thing to do is to convert travel survey trip records into origin-destination pairs with a zoning system. A typical OD flow dataset looks like the below.


| Origin zone  | Destination zone | Trip number |
| ------------- | ------------- | ------------- |
| 100  | 100  | 45  |
| 101  | 100  | 78  |
| 100  | 101  | 22  |
| 101  | 114  | 1  |


After making the zone id just like the zoning system, there is a great tutorial on how to generate OD polylines with the origin and destination of each connection consistent with their polygons' centroid.

> [Origin-destination data with stplanr](https://cran.r-project.org/web/packages/stplanr/vignettes/stplanr-od.html)

## A Shiny app
Shiny is a web application framework for R. It allows you to quickly create your web-based data product. You can create one inside RStudio and fill in the below two scripts.

### ui.R
I show the skeleton of the script here for clarity. The layout can be found [here](https://shiny.rstudio.com/articles/layout-guide.html) as a start. More detailed description of the control widgets can be found [here](https://shiny.rstudio.com/tutorial/written-tutorial/lesson3/).

```r
library(shiny)
library(dplyr)
library(sf)
library(stplanr)
library(tmap)

# Define UI for application that draws a OD network
shinyUI(fixedPage(

    # Application title
    titlePanel("Origin-destination matrices (ODMs) explorer"),

    sidebarLayout(
        sidebarPanel(
            radioButtons("mode", ...),

            radioButtons("time", ...),
            h5("No will show the results of all trips over 24 hours."),
            hr(),
            conditionalPanel("input.time == 1",...),

            submitButton("Plot"),
            ...
        ),

        mainPanel(
            ...,

            plotOutput("netPlot", height = "800px", width="100%"),

            ...
        )
    )
))
```
### server.R


[^1]: I've been taking [Data Science Specialization](https://www.coursera.org/specializations/jhu-data-science) on Coursera. This post is based on the final project of Course 9/10 [Developing Data Products](https://www.coursera.org/learn/data-products).
