---
layout: post
title: "Discussion"
subtitle: "How can we classify our results"
date: 2023-02-31 10:45:13 -0400
background: '/img/posts/06.jpg'
author: Maria Riegel
---
# Note
* https://github.github.com/gfm/
# Ideas

**Juliette:**
* could we reach our goal : more or less still need to train, if the model is training it should be ablo to generate building footprints for cities with less density than Singapor or Paris
* limitations :
    *   size of the tiles + zoom --> depends on the city's morphology example with Jakarta
    * streets that we should include or not in our streetnetwork map 

**Jonathan:**
* bad description how to preprocess the training data
* no full training since the limited amount of ressources
* not conducting the second approach
* populaiton density as an indicaiton for the amount of building footprints
* pixel distribution -> since streets are included and this could to false training -> better would to use just buildings than include streets & train
* testing more parameters -> we did not test all hyperparameters
* we did not slightly change the model, but is really important to get the best results
* completness of the osm data -> especially on more rare street types + we did not checked if the hierachy is complete + also buildings are partly build but not in the osm data
* adaption of the discussion in the data section -> why was it a 'bad' idea to use population density as a proxy for city morphology -> this could be argued with the funcitoning of the model + also the amount training data
* Should we include more than 3 classes for population density or in total a different apprximation method -> is pixel a better way? -> maybe yes in terms of model but worse regarding our topic  
