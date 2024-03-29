---
title: "Exploring nativity segregation in Sweden with big geolocation data on human mobility"
date: 2023-07-24
summary: "Presentation at the 9th International Conference on Computational Social Science (Copenhagen, Denmark | July 17-29, 2023)."

tags: ["R", "transport", "mode", "origin-destination matrix", "Shiny"]

image:
  caption: Presenting at Session Mobility and Urban Data Science IV
  focal_point: Smart
---

I am excited to share my recent experience presenting at the 9th International Conference on Computational Social Science, where I had the opportunity to connect with a fascinating and rapidly growing community of human mobility and social segregation in urban analytics and computational social science. This study investigates the below two research questions:

- How is experienced nativity segregation different from residential nativity segregation?
- What are the impacts of income level and transport accessibility on experienced nativity segregation by individuals?

Download the slides {{% staticref "uploads/slides_IC2S22023_Yuan Liao.pdf" "newtab" %}}here{{% /staticref %}}.

Access the interactive map [here](https://yuanliao.shinyapps.io/InteractiveVisiSegSweden/), where you can play with the census statistics and the results from our study.

{{< figure src="screenshot.jpg" title="Screenshot of the interactive data visualization." >}}

{{% callout warning %}}
Please note this is an ongoing study. The results may change depending on the evolving research focus and the analysis methods.
{{% /callout %}}

## Nativity Segregation in a Polarized World

Nativism often leads to the clustering of people from different birthplaces into distinct communities, potentially causing negative impact on social cohesion and integration. This study aimed to shed light on the extent and implications of nativity segregation in Sweden, a country known for its ever-increasing segregation level since 1990.

## Leveraging the Power of Big Geolocation Data on Human Mobility

Quantifying social segregation using spatiotemporal approaches becomes feasible thanks to increasingly available mobility data from large populations. Although being in the same place (co-presence) does not always lead to social interactions, human mobility data provides a more realistic approximation of potential and actual interactions between groups.

Using geolocation data collected from a large population in Sweden (2019), this study looked at experienced nativity segregation in a comparison with the traditional static view i.e., residential segregation. Specifically, we examined the separation between foreign-born outside Europe vs. native-born populations.

## Key Findings
- Nativity segregation is still evident in various urban centers and regions across Sweden.
- When considering mobility, individual's experienced nativity segregation deviates from his/her residential segregation, calling for this more comprehensive approach driven by real-world data.
- Compared with the foreign-born, the native-born residents are more capable of reducing their nativity segregation level by moving toward places that are more diverse.
- Decreased nativity segregation when people move outside their home is associated with better transport access. But car and transit have different association patterns depending on foreign/native-born.

## Outlook
By addressing the drivers of segregation, we can pave the way for more sustainable and harmonious societies. By expanding the analysis to include a holistic set of explanatory variables such as mobility patterns and housing, we can gain a more nuanced understanding of nativity segregation and its evolving nature. Going from there, we can contribute to inclusive spatial planning.

## Remarks
This is the first study of our [MobiSegInsights project](https://github.com/MobiSegInsights) put together by a list of amazing researchers. It is my true honor to work with them.

Attending this conference also opens up exciting avenues for future investigations. A non-exhaustive list of relevant contributors from this conference is summarized below. You may also like their projects and papers if you are interested in our work.

### Social Segregation / Social Mixing / Inequalities
Understanding urban social resilience through behavioral mobility data. [Keynote](https://www.ic2s2.org/keynotes.html#esteban) by _Esteban Moro_.

#### Using Empirical Mobility/Place Data
Disaggregating bike-share mobility data to measure urban segregation over time ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper877.pdf)). _David Mingfei Liu_

Mobility Connectedness: Uncovering socioeconomic bias and connectivity in urban mobility ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper700.pdf)). _Damin Lee, Ohhyun Kwon, Inho Hong, Jaehyuk Park, Woo-Sung Jung, Hyejin Youn_

How Can Transport Inequality Contribute to Housing Insecurity? ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper361.pdf)). _Nandini Iyer, Ronaldo Menezes, Hugo Barbosa_

Mobility and Transit Segregation in Urban Spaces. ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper362.pdf)). _Nandini Iyer, Ronaldo Menezes, Hugo Barbosa_

Network analysis reveals fare-free shared bike system improves community integration in Boston ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper135.pdf)). _Nail Furkan Bashan, Qi Wang_

Social-economic segregation dynamics at neighborhoods scale ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper631.pdf)). _Lavinia Rossi Mori, Vittorio Loreto, Riccardo Di Clemente_

Amenity complexity and urban locations of socio-economic mixing ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper40.pdf)). _Sandor Juhasz_

Idiosyncratic and systematic experienced isolation in urban networks ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper446.pdf)). _Andrew Renninger_

#### Theoretical Models
A Mobility-constrained Segregation Model ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper385.pdf)). _Daniele Gambetta, Luca Pappalardo, Giovanni Mauro_

Urban scaling laws arise from within-city inequalities ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper241.pdf)). _Martin Arvidsson, Marc Keuschnigg_

### Other Studies Using Big Geolocations on Human mobility
Understanding the gender gaps in employment and mobility using large-scale behavioral data ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper73.pdf)). _Silvia De Sojo Caso, Sune Lehmann, Laura Maria Alessandretti_

Uncovering the differences and similarities between physical and virtual mobility ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper456.pdf)). _Surendra Hazarie, Hugo Barbosa, Adam Frank, Ronaldo Menezes, Gourab Ghoshal_

Comparing Methodologies for Constructing Epidemic Networks from GPS Mobility Data ([abstract](https://laura.alessandretti.com/public/pdf_accepted/paper904.pdf)). _Francisco Barreras, Bethany Hsiao, Duncan J Watts_
