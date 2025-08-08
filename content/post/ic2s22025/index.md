---
title: "Mobility and Urban Science in Computational Social Science"
date: 2025-08-08
summary: "Organizing the 11th International Conference on Computational Social Science (Norrköping, Sweden | July 21-24, 2025)."

tags: ["academic services", "urban science", "computational social science"]

image:
  caption: IC2S2 2025 (screenshot from the website)
  focal_point: Smart
---

The 11th International Conference on Computational Social Science took place in Norrköping, Sweden, July 21–24, 2025 ([website](https://www.ic2s2-2025.org/)). I'm deeply honored to have been part of the organizing team.

{{< figure src="team.jpg" title="Organizing team (Photo credit - Vsevolod Suschevskiy)." >}}

As a transport researcher, my path into computational social science has been full of eye-opening moments. In a world where disciplinary boundaries keep blurring, IC2S2 showcases how diverse communities come together to form a strong, inspiring "big family."

My work sits at the intersection of transport, mobility data science, and urban science. A project on socio-spatial segregation and human mobility has brought me into close collaboration with computational social scientists, physicists, and complex systems researchers. In day-to-day research, we're much closer than we think—transport scholars, computational social scientists, and others can work together smoothly and keep inspiring each other.

Special thanks to my colleague Josef Ginnerskov, who modeled topic themes from this year's submissions and produced a fantastic visualization. Large Language Models (LLMs) feature prominently, serving as a connective thread that bridges diverse themes.

{{< figure src="cloud.png" title="Topics of IC2S2 2025 submissions by Josef Ginnerskov." >}}

One cluster that especially resonates with my interests is Mobility & Urban Life. I'll zoom in on that topic cloud and share a few insights from the accepted papers presented at the conference. You can also find a list at the end of this article.

Relevant to my research focus on segregation, social mixing, and spatial inequality, there are a few studies about barriers, exposure, and who meets whom where, featuring the application of large amount of geolocation data. For example, Aiello et al. (2025) overlays highway networks with a massive Twitter follower graph across 50 U.S. metros to compute a Barrier Score, showing highways systematically suppress cross-neighborhood social ties—most strongly within ~5 km—and flagging corridors with long-lived segregation effects [118]. Rosen et al. apply Cuebiq mobility across 11 U.S. metro areas to measure how socioeconomic integration fluctuates over the day—across cities, within cities, and by POI type—showing places that look integrated at one time can be segregated at another [340]. Samaniego et al. build SES-tagged call networks from Chile and Brazil and, using a modified exposure index, find robust socioeconomic homophily, with main network components showing more cross-SES interaction than full networks [429]. Renninger analyzes visits to ~5 million POIs with counterfactuals to show downtowns drive more socioeconomic mixing than "bridge" amenities would predict—and that pandemic remote work cut such mixing by ~8% [561].

Across the other part of the collection, studies span disasters and resilience. For example, Naushirvanov et al. use mobile network data and alert timing to unpack evacuation and short-term displacement in the 2024 Valparaíso wildfires, revealing SES-linked differences in response [711]. In accessibility and transport policy, Cornacchia et al. introduce DiverCity to quantify route diversification and show how network topology and mobility attractors shape efficiency [418]. Climate and environment related work such as the one by Renninger measures how extreme heat suppresses mobility in Spain, with heterogeneous impacts by age and income [532]. Methods papers like the one by Bison et al. advances data quality and sensing, integrating UWB/Bluetooth wearables, smartphone diaries, and surveys to capture dynamic social contacts [266]. Fujimoto et al. advances AI for urban analysis by fusing a Vision Transformer with GPT-2 to generate realistic mobility trajectories from map context [386]. Migration research such as the one by Robiglio et al. applies network clustering to Austrian internal moves, surfacing administrative-boundary and urban–rural effects beyond gravity models [425]. Well-being studies like the one by Bergmann et al. link smartphone-tracked activity patterns to life satisfaction using interpretable ML across multiple countries [930].

## Remarks
Two years after my last IC2S2 in Copenhagen, our socio-spatial segregation and mobility project has produced two papers and a preprint on segregation, social mixing, and spatial inequality ([project](https://github.com/MobiSegInsights)). Check them out:

Liao, Yuan, et al. "The effect of limited mobility on the experienced segregation of foreign-born minorities." npj Sustainable Mobility and Transport 2.1 (2025): 29. [[Link](https://www.nature.com/articles/s44333-025-00046-4)]

Liao, Yuan, et al. "Socio-spatial segregation and human mobility: A review of empirical evidence." Computers, Environment and Urban Systems 117 (2025): 102250. [[Link](https://doi.org/10.1016/j.compenvurbsys.2025.102250)]

Liao, Yuan, et al. "Uncovering the Social and Spatial Effects of Fare Cuts on Public Transport with Mobile Geolocation Data." Available at SSRN 5179427. [[Link](https://dx.doi.org/10.2139/ssrn.5179427)]

Until next time.

## Presented papers in mobility and urban science
593 Comparing mobile phone and facebook data during emergencies (#593; Poster ID: 23) _Timur Naushirvanov, Erick Elejalde, Elisa Omodei, Kyriaki Kalimeri, Marton Karsai, Leo Ferres_

260 AI for Spatial Justice: Multimodal and Street View Imagery Uncover Waste Disparities in Nairobi’s Informal Settlements (#260; Poster ID: 50) _Wenlan Zhang, Chen Zhong, Qunshan Zhao_

531 Introducing a new dataset for conflict damage prediction (#531; Poster ID: 51) _Clara-Gabriela Clipea_

266 Reconstructing Interactional Networks through Wearable Proximity Sensors and Digital Time Diaries (#266; Poster ID: 54) _Ivano Bison, Tommaso Trulli, Amy L Murphy, Davide Molteni, Gian Pietro Picco, Michele Tizzoni_

305 Analyzing activity patterns during EV charging sessions using mobility data (#305; Poster ID: 55) _Callie Clark, Xiyuan Ren, Salsabil Salah, Anne Driscoll, Joseph Chow, Takahiro Yabe_

88 Geospatiality of Topics in English Text Data (#88; Poster ID: 105) _Johannes Mast, Christian Geiß, Hannes Taubenböck_

418 Route diversification in road networks (#418; Poster ID: 3) _Giuliano Cornacchia, Luca Pappalardo, Mirco Nanni, Dino Pedreschi, Marta C. Gonzalez_

1054 Spatial Mobility and Housing Demand in a Dynamic Microsimulation Model (#1054; Poster ID: 80) _Sarah Bohnensteffen_

425 Mesoscopic description of deviations from gravity models in Austrian migration flows (#425; Poster ID: 82) _Thomas Robiglio, Martina Contisciani, Marton Karsai, Tiago P. Peixoto_

945 A Synthetic Dataset and Framework to Test Pre-processing Algorithms of Human Mobility Data (#945; Poster ID: 83) _Thomas H. Li, Francisco Barreras, Duncan J. Watts_

561 The (changing) role of central places in ameliorating exposure segregation (#561; Poster ID: 86) _Andrew Renninger_

930 Digital Traces of Well-Being: Satisfaction with Life Manifests in Everyday Physical Activity Captured with Smartphones (#930; Poster ID: 96) _Maximilian Bergmann, Sarah Marie Müller, Ramona Schoedel, Gabriella Harari, Mirjam Stieger, Markus Buehner, Samuel Gosling, Mathias Allemand, Clemens Stachl_

764 The Digital Authoritarian: Everyday behavioral patterns collected with smartphones predict authoritarianism (#764; Poster ID: 5) _Timo Koch, Sanaz Talaifar, Daniel Racek, Jan Digutsch, Pietro Alessandro Aluffi, Ramona Schoedel, Markus Buehner, Clemens Stachl_

199 Causal Inference in the City: Evaluation of Policy Interventions' Impact using Mobility Networks (#199; Poster ID: 92) _Bijin Joseph, Hamish Gibbs, Takahiro Yabe, Esteban Moro_

429 Socioeconomic Segregation in Voicecall Networks: Analyzing the Impact of City Size in Chile and Brazil (#429; Poster ID: 95) _Horacio Samaniego, Joaquín Ignacio Villagra Pacheco, Yerka Freire, Alexandre Evsukoff_

456 Impact of Temporary Location Visitors on Mobile App Usage in French Cities: Implications for Socio-Economic Segregation Studies (#456; Poster ID: 97) _Egor Kotov, Tom Theile, Ole Hexel, Elizabeth Jacobs, JISU KIM, Daniela Perrotta, Emilio Zagheni_

248 Cascades of violence: Identifying armed conflict archetypes through data (#248) _Niraj Kushwaha_

83 From Occasional to Steady: Habit Formation Insights From a Comprehensive Fitness Study (#83) _Onur Varol, Ege Demirci, Efe Tüzün, Ahmet Furkan Ün, taners_

206 Generative Multimodal Models for Social Science: An Application with Satellite and Streetscape Imagery (#206) _Tina Law, Elizabeth Roberto_

418 Route diversification in road networks (#418) _Giuliano Cornacchia, Luca Pappalardo, Mirco Nanni, Dino Pedreschi, Marta C. Gonzalez_

764 The Digital Authoritarian: Everyday behavioral patterns collected with smartphones predict authoritarianism (#764) _Timo Koch, Sanaz Talaifar, Daniel Racek, Jan Digutsch, Pietro Alessandro Aluffi, Ramona Schoedel, Markus Buehner, Clemens Stachl_

386 Generation of Human Mobility Trajectories Using Map Information (#386) _Shouji Fujimoto, Atushi Ishikawa, Takayuki Mizuno_

532 Extreme heat reshapes daily travel behaviour (#532) _Andrew Renninger_

48 When Proximity Falls Short: Inequalities in Commuting and Accessibility in Santiago (#48) _Cesar Marin-Flores, Leo Ferres, Henrikki Tenkanen_

1013 Exploring Multidimensional Accessibility and Flow Patterns in Urban Commercial Areas (#1013) _Minjin Lee, Hyoji Choi, Taesung Hwang, Jeong hwan Jeon_

118 Urban highways are barriers to social ties (#118) _Luca Maria Aiello, Anastassia Vybornova, Sandor Juhasz, Michael Szell, Eszter Bokanyi_

55 Decomposing geographical and universal aspects of human mobility (#55) _Louis Boucherie, Benjamin Frank Maier, Sune Lehmann_

827 The Effect of Trajectory Sparsity on Epidemic Modeling Outcomes (#827) _Federico Delussu, Francisco Barreras, Yuan Liao, Laura Maria Alessandretti, Duncan J. Watts_

28 Technological Change Shapes the Geometry of Urban Evolution (#28) _Ziyu Chen_

1022 Working behaviour and the spatial complexity of economic activity (#1022) _Zsófia Zádor, Balázs Lengyel, Riccardo Di Clemente_

340 The temporal dimension of experienced segregation in cities (#340) _Joshua Rosen, Brennan Klein, Erik Weis, Hamish Gibbs, Daniel O’Brien, Takahiro Yabe, Esteban Moro_

525 Structural differences in gendered mobility networks (#525) _Silvia De Sojo, Sune Lehmann, Laura Maria Alessandretti_

301 Incorporating Social Influence in LLM-Agent Based Modeling Improves Predictability of Evacuation (#301) _DongHak Lee, Jiayi Weng, Vaidehi Raipat, Takahiro Yabe_

711 Behavioral response to mobile phone evacuation alerts (#711) _Timur Naushirvanov, Erick Elejalde, Kyriaki Kalimeri, Elisa Omodei, Marton Karsai, Leo Ferres_

155 Social homophily predicts evacuation destination choice and long-term displacement (#155) _Vaidehi Raipat, Takahiro Yabe_

686 Urban Safety Perception Through the Lens of Large Multimodal Models: A Persona-based Approach (#686) _Ciro Beneduce, Massimiliano Luca, Bruno Lepri_

508 Uncovering Urban Lifestyles Through Detailed Large-scale Purchase Records (#508) _Minjin Lee, Hokyun Kim, Bogang Jun, Jaehyuk Park_

643 Social network communities and income convergence in the largest US cities (#643) _Imre Gémes, Eszter Bokanyi, Sandor Juhasz, Balázs Lengyel, Gergo Toth_

73 Forecasting Nationwide Crime at the Block Level (#73) _Kenji Yokotani, Nobuhito Abe, Masahiro Takamura_

808 One Map, Many Trials: Overcoming Bias and Uncertainty in Satellite-Based Poverty Maps for Reliable Impact Evaluation (#808) _Markus Bo Pettersson, Connor Thomas Jerzak, Adel Daoud_

761 Quantifying world geography as seen through the lens of Soviet propaganda (#761) _Mikhail Tamm, Mila Oiva, Maximilian Schich, Mark Mets, Ksenia Mukhina_