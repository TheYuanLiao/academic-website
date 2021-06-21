---
title: "Doctoral thesis successfully defended"
date: 2021-06-21
summary: "Doctoral thesis, slides, and source code of slides via ioslides."

tags: ["dissertation", "presentation", "R", "ioslides"]

image:
  caption: Photo by Yuan Liao
  focal_point: Smart
---

After four-year research (08-15-2017 -- 06-16-2021), I successfully defended my doctoral thesis online at Chalmers University of Technology, Gothenburg, Sweden. My thesis is in the field of mobility data science: [Understanding Mobility and Transport Modal Disparities Using Emerging Data Sources: Modelling Potentials and Limitations](https://research.chalmers.se/en/publication/523982). Below is a Tweet thread from my dear supervisor, Sonia Yeh.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Congrats to <a href="https://twitter.com/TheYuanLiao?ref_src=twsrc%5Etfw">@TheYuanLiao</a> for defended ur thesis. The Grading committee <a href="https://twitter.com/SiiriSilm?ref_src=twsrc%5Etfw">@SiiriSilm</a> <a href="https://twitter.com/IsabLThomas?ref_src=twsrc%5Etfw">@IsabLThomas</a> <a href="https://twitter.com/gissong?ref_src=twsrc%5Etfw">@gissong</a> John Östh, Opponent <a href="https://twitter.com/jmichaelbatty?ref_src=twsrc%5Etfw">@jmichaelbatty</a> were unanimously impressed w/ ur work on big data and mobility. What better way to celebrate than to mark this event with a geotagged tweet! <a href="https://t.co/SQnQviVXRU">https://t.co/SQnQviVXRU</a></p>&mdash; Sonia Yeh (@Sonia_Yeh) <a href="https://twitter.com/Sonia_Yeh/status/1405187629235253248?ref_src=twsrc%5Etfw">June 16, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

It was a long but exciting process to talk about my doctoral research; a 30-min presentation followed by the questions from the opponent and the four committee members. I enjoyed it a lot! I will continue exploring the many possibilities in the field of mobility data science as a postdoctoral researcher working together with my former supervisors, Sonia Yeh and Jorge Gil.

But this post is more than announcing the great news. I include the source code of making a presentation using ioslides, given I experienced the whole learning process in preparing my dissertation presentation. Hope you find it helpful.

## Dissertation slides made by ioslides

My dissertation slides available [here](https://theyuanliao.github.io/dissertation.html).

In preparing for the PhD defense, I decided to learn some new technique of making slides to add more fun. Eventually, I used ioslides by R. However, it was not an easy and smooth process by just looking at the basic tutorial from the [official documentation](https://bookdown.org/yihui/rmarkdown/ioslides-presentation.html). To make a decent ioslides presentation for academic purposes, one may need a hybrid use of html and rmarkdown.

You can access the source code of making my slides using R ioslides [here](https://github.com/TheYuanLiao/dissertation).

The source code solves the issues of making footnote, customising style e.g., changing background, logo, and removing the default gray bottom, inserting emojis, incremental bullet points, inserting html tables, and most important, flexible floating segments (of pics/bullet points/tables etc).
