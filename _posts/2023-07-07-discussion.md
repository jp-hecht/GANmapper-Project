---
layout: post
title: "Discussion"
subtitle: "How can we classify our results"
date: 2023-07-30 11:45:20 -0400
background: '/img/hh3.jpg'
author: Maria Riegel
---
> Headings? Sections? Maybe not necessary
>
> that also correspond to reality -> what do you mean with that?
>
> computer computing time -> just computing time
>
> not only limited time period -> also especially the necessary computing units are missing

The aim is to generate true-to-scale and true-to-angle building ground plans of other cities that also correspond to reality. So far, the planned goal has not been achieved. One reason may be insufficient training of the model with the data. If the model were trained with the new data over a longer period of time, it should be able to generate building footprints for cities with a lower population density than Singapore or Paris. The calculation of the model is also associated with a long computer computing time, which has made multiple training even more difficult for the limited time period.


> Floor plans? -> building footprints?
>
> We again

We also reached its limits when generating the floor plans. There were limitations with the size of the tiles. The zoom factor cannot be freely selected, but depends on the morphology of the city. Another problem arose from the city's road network. It was unclear which streets we should or should not include in our street network map. By having too many streets in a large scale, it was difficult to distinguish the streets from each other. The larger the zoom factor, the more obvious it was to use fewer roads and rather use federal or motorway roads to ensure the clarity to assign the individual tiles. The smaller the zoom factor, the more suitable it was to use main and secondary roads from the 30 km zone.   

> Very helpful -> not scientific 
>
> zoom factor was described -> road network not 

In general, the report by Abraham Wu and Filip Biljecki is insufficient in describing the use and processing of the training data. An additional description of how the training data was processed, which zoom factor or which road network was used would have been very helpful for our elaboration.

> every town -> do you mean the administrative units or distric
> 
> building ground plans?
>

Likewise, we have reached its limits in the search for suitable data. On the one hand, there are not freely available data sets on buildings or street networks for every town in Germany. In the federal state of Schleswig-Holstein, for example, there is an internet site with a complete data set on building ground plans for every district, whereas in Hamburg you have to apply for information on the official real estate cadastre via the State Office for Geodesy and Surveying. For other regions, we have found that the freely available data is not up-to-date or incomplete, as buildings or streets were sometimes missing in the data comparison with Google Maps. The problem occurred more often with roads than with buildings. One reason for this could be the imprecise hierarchy of the streets and the lack of up-to-dateness. This also limits the resources for a realistic creation.

The second planned approach for our analysis using population density as an indicator for the size of the building footprint could not be carried out and the idea had to be discarded. The reason for this is that population density cannot be used as an indicator. Large cities live from work and therefore many buildings are available as office space and are not directly inhabited. Therefore, population density is not optimal as an indicator for building floor space. On the other hand, population density also does not fit the way the model works and the amount of trainig data that can be used.

Pixel distribution is a relevant factor that must be taken into account. It was found that wrong roads are included in the dataset and thus also lead to wrong training. It has been found that it would be better to use only buildings than to include roads for processing the data.

> it is not relevant if the understanding of the parameters is hard !

A lot of parameters are used in the source code, which are not particularly discussed in the article. There is no description of all the parameters used, so it is not easy to understand them. Some of the parameters can be identified by their names and used for the new model. We were able to test and adjust a few parameters. A short explanation of the parameters used would have been very desirable and would also have opened up more possibilities for editing. In the end, not all hyperparameters could be tested and were left at their default settings.  


> please don't say that we did not understood the model fully if you say so our whole work is obsolete

Overall, the whole model was hardly changed, except for a few selected parameters, the input data and the output location. To achieve the best results, it would be better to understand the entire model completely in order to achieve the best results in the end.
