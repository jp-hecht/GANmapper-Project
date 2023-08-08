---
layout: post
title: "Discussion"
subtitle: "How can we classify our results"
date: 2023-07-30 11:45:20 -0400
background: '/img/hh3.jpg'
author: Maria Riegel
---

The aim is to generate building footprints of other cities that are true to scale and angle and that also correspond to reality in terms of completeness and accuracy. So far, the planned goal has not been achieved. One reason may be insufficient training of the model with the data. If the model were trained with the new data over a longer period of time, it should be able to generate building footprints for cities with a lower population density than Singapore or Paris. The calculation of the model is also associated with a long computing time, which has made multiple training even more difficult for the limited time period. In particular, the necessary computational units are also lacking.
>
>
We also reached its limits when generating the building footprints. There were limitations with the size of the tiles. The zoom factor cannot be freely selected, but depends on the morphology of the city. Another problem arose from the city's road network. It was unclear which streets we should or should not include in our street network map. By having too many streets in a large scale, it was difficult to distinguish the streets from each other. The larger the zoom factor, the more obvious it was to use fewer roads and rather use federal or motorway roads to ensure the clarity to assign the individual tiles. The smaller the zoom factor, the more suitable it was to use main and secondary roads from the 30 km zone.
>
>
In general, the report by Abraham Wu and Filip Biljecki is insufficient in describing the use and processing of the training data. There is no additional description of how the training data was processed and which road network was used.
Likewise, the search for suitable data has reached its limits. On the one hand, there are not freely available data sets on buildings or road networks for every city in Germany. In the federal state of Schleswig-Holstein, for example, there is an internet site with a complete data set on building footprints for every district, whereas in Hamburg one has to apply for information on the official real estate cadastre via the State Office for Geodesy and Surveying. For other regions, it had to be determined that the freely available data is not up-to-date or incomplete, as buildings or streets were sometimes missing in the data comparison with Google Maps. However, building plans for some regions are published on the internet and can be accessed. The problem has occurred more often with roads than with buildings. One reason for this may be the imprecise hierarchy of roads and the lack of up-to-dateness. This also limits the resources for a realistic creation.
>
>
The second planned approach for our analysis using population density as an indicator for the size of the building footprint could not be carried out and the idea had to be discarded. The reason for this is that population density cannot be used as an indicator. Large cities live from work and therefore many buildings are available as office space and are not directly inhabited. Therefore, population density is not optimal as an indicator for building floor space. On the other hand, population density does not fit the functioning of the model and the amount of training data that can be used.
Pixel distribution is a relevant factor that must be taken into account. It was found that wrong roads are included in the data set and thus also lead to wrong training. It has been found that it would be better to use only buildings than to include roads for processing the data.
>
>
A lot of parameters are used in the source code, which are not particularly discussed in the article. There is no description of all the parameters used, so it is not easy to understand them. Some of the parameters can be identified by their names and used for the new model. A few parameters could be tested and changed. In the end, not all hyperparameters could be tested and were left at their default settings.
>
>
Overall, the whole model was hardly changed, except for a few selected parameters, the input data and the output location. To achieve the best results, it would be better to change more parameters and test the new training data set again and again with new input parameters until the best results are achieved.
