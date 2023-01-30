# Sennosen
A framework for easy timeseries analysis experiments

![Overall View](https://github.com/H202Woo/sennosen/blob/main/img/Overall1.jpg "SNS")

## Motivation
Timeseries data analysis is an incredible topic. There are so many algorithms around and such a vivid community. Understand the underlying forces driving the macroscopic effect measured converts data into knowledge. Next, extrapolate these learnings enable users to reach one of the golden goal : data forecasting.

No matter the language used, many libraries have been and are still published to support such investigations. Often libraries are released aside with their published research papers or use cases are investigated and related by reaserchers into web blogs. A current trend for such data analysis blogs is to supply references to a Jupyter notebook to illustrate the purpose of the resaerch area. This enables a peer validation and allows reusability for the reader.

"_But what if we want to experiment these methodologies on our own dataset ?_"

"_What if we want to combinate data treatments into a complex data pipeline ?_"

"_What if we need to saerch for the right approach applicable to our context of data ?_"

This is **Sen-no-sen**'s purposes:
- for the users : offer a data analysis experimentation playground with many tools that can be easily combined into analysis recipes
- for the researchers : give the possibilty to publish or demo their algorithm as ready-to-go analysis block
- for the curious : propose a framework to learn data analysis with hands-on aside with theoritical background thanks to the contextual documentation

## Quick Start
1. Click on the vertical tabs to hide/show the panes:
    - the toolbox : this is where the tools are sorted. Pick a tool and drop it on the analysis pane
    - the analysis : the analysis recipe is displayed as nested building blocks (tools)
    - to access to the documentation pane on the right : get some help and theoritical background on the tool (to come)

2. Click on any tool to display its help file in the documentation pane.
3. Drop any tool on the analysis pane and build your analysis recipe/pipeline
4. Hit Generate to display the result

## Recipe rules
A recipe is built by laying down blocks/tools in a particular configuration. When a tool is dropped onto another one a hierarchical tree is built. The nested tool becomes the child of the previous and inherits of its parent context. The context consists of every data and parameters set by its parent tool. Hence a complete analysis recipe is seen as successive operations performed by the children tools on its parent context.

Tools are grouped by family (datasources, extract, transform, view, analyze, detection, forecast, etc.) and some rules are enforced to guarantee a coherent recipe structure. As an example, datasource may only be dropped as the first tool. In turn, extractors tools are always defined as children of a datasource where they get their data from.
When bulding the recipe, the mouse cursor  guides you with the rules by disabling you to drop the tool on an inapropriate parent.

A typical recipe for an analysis starts from the configuration of a datasource as a provider for the data. On the provider an extractor tool is used to narrow the data of interest by setting the tags to analyse and the time period. The dataset is queried from the parent context.

![](https://github.com/H202Woo/sennosen/blob/main/img/Silverkite%20forecasting%201.jpg "")

# Installation instructions
to come

# Next steps
to come

## Why Sen-no-sen ?

Sen-no-sen (先の先); is a term taken from the japanese martial arts. It litteraly translates as "ahead" but is often extended to "initiave". In this context it means "to take the intiative (of the attack) just before the opponent initiates any movement".
During trainings each opponents throw their souls into the perception of every single movement, sign or intention to attack in order to react accordingly. The name sen-no-sen has been selected for this project as it aims to build a playground for forecasting and data timeserie analysis.

