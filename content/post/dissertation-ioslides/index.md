---
title: "Doctoral thesis defended and some tricks about making ioslides"
date: 2021-06-21
summary: "Doctoral thesis, slides, and how-to about making ioslides."

tags: ["dissertation", "R", "ioslides"]

image:
  caption: Photo by Yuan Liao
  focal_point: Smart
---

**Doctoral thesis successfully defended**

After four-year research (08-15-2017 -- 06-16-2021), I successfully defended my doctoral thesis online at Chalmers University of Technology, Gothenburg, Sweden. My thesis is in the field of mobility data science: [Understanding Mobility and Transport Modal Disparities Using Emerging Data Sources: Modelling Potentials and Limitations](https://research.chalmers.se/en/publication/523982). Below is a Tweet thread from my supervisor.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Congrats to <a href="https://twitter.com/TheYuanLiao?ref_src=twsrc%5Etfw">@TheYuanLiao</a> for defended ur thesis. The Grading committee <a href="https://twitter.com/SiiriSilm?ref_src=twsrc%5Etfw">@SiiriSilm</a> <a href="https://twitter.com/IsabLThomas?ref_src=twsrc%5Etfw">@IsabLThomas</a> <a href="https://twitter.com/gissong?ref_src=twsrc%5Etfw">@gissong</a> John Östh, Opponent <a href="https://twitter.com/jmichaelbatty?ref_src=twsrc%5Etfw">@jmichaelbatty</a> were unanimously impressed w/ ur work on big data and mobility. What better way to celebrate than to mark this event with a geotagged tweet! <a href="https://t.co/SQnQviVXRU">https://t.co/SQnQviVXRU</a></p>&mdash; Sonia Yeh (@Sonia_Yeh) <a href="https://twitter.com/Sonia_Yeh/status/1405187629235253248?ref_src=twsrc%5Etfw">June 16, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>



## Dissertation slides made using ioslides [^1]

The dissertation slides is available below.

{{< minipage "https://theyuanliao.github.io/dissertation.html" >}}

## Some tricks about making ioslides
Shiny is a web application framework for R. It allows you to quickly create your web-based data product. You can create one inside RStudio and fill in the below two scripts.

### ui.R
Below is the skeleton of the script for clarity. A tutorial for beginners of Shiny layout can be found [here](https://shiny.rstudio.com/articles/layout-guide.html). More detailed description of the control widgets can be found [here](https://shiny.rstudio.com/tutorial/written-tutorial/lesson3/).

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

{{% callout note %}}
`submitButton` is particularly useful when the data size is big. Prepare input and hit the plot button to see the results.
{{% /callout %}}

### server.R
We now fill in what to do with the `input` to produce the `output` inside `shinyServer(function(input, output){...})`. All the loaded libraries and created variables in ui.R and server.R are sharing the same environment.

{{% callout note %}}
Please make sure that the data used are stored under your App folder and published together with everything else. Use the relative path to access it. `data/file2use.csv` instead of `../../data/file2use.csv`.
{{% /callout %}}

#### 1 Load OD data and preprocess
The first step inside `shinyServer(function(input, output){...})` is to load data and preprocess.

```r
df <- read.csv('data/odms_by_mode.csv')
zones <- st_transform(st_read('data/zones_subset.shp'), crs = 4326)
colnames(df) <- c("ozone", "dzone", "Non-bike", "E-bike", "Bike", "Total", 'Hour')
df <- df %>% filter(ozone %in% zones$zone, dzone %in% zones$zone)
```

#### 2 Prepare data based input in ui.R
Taking all the input, `mode`, `time`, and `hour`, the below chunk subsets the data and creates Polylines using the R package [`stplanr`](https://docs.ropensci.org/stplanr/).

```r
odm <- reactive({
    # Subset data based on input$mode and input$hour from ui.R
    md <- input$mode
    hr <- ifelse(input$time == 0, 24, input$hour)
    df_a <- df %>%
        select(c('ozone', 'dzone', !!md, 'Total', 'Hour')) %>%
        filter(ozone != dzone,
               Hour == hr) %>%
        mutate(trip = get(md) / sum(get(md)) * 100) %>%
        filter(trip > 0) %>%
        mutate(share = get(md) / Total * 100)

    # Create lines between OD zones
    lines <- od2line(flow = df_a, zones = zones)
    lines <- arrange(lines, trip)
    return(lines)
})
```

{{% callout note %}}
`odm` is a function to be called later.
{{% /callout %}}

#### 3 Prepare data based input in ui.R
Finally, we are ready to plot the OD network using R package [`tmap`](https://cran.r-project.org/web/packages/tmap/vignettes/tmap-getstarted.html).

```r
output$netPlot <- renderPlot({
    # draw the ODMs
    tm_shape(zones) +
        tm_fill(col="grey35") +
        tm_borders("white", alpha=.2) +
        tm_shape(odm()) +
        tm_lines(
            palette = "plasma",
            trans = "log10", style="cont",
            lwd = "trip",
            scale = 9,
            title.lwd = 0.5,
            alpha = 0.5,
            col = "share",
            title = "Mode share (%)",
            legend.lwd.show = FALSE
        ) +
        tm_scale_bar() +
        tm_layout(
            title = input$mode,
            frame = FALSE,
            legend.bg.alpha = 0.5,
            legend.bg.color = "white"
        )
})
```
[^1]: Source code on [GitHub](https://github.com/TheYuanLiao/dissertation).
