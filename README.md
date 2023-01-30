# Sennosen
A framework for easy timeseries analysis experiments

![Overall View](https://github.com/H202Woo/sennosen/blob/main/img/Overall1.jpg "SNS")

## Motivation
Timeseries data analysis is an incredible topic. There are so many algorithms around and such a vivid community. Understand the underlying forces driving the macroscopic effect measured converts data into knowledge. Next, extrapolate these learnings enable users to reach one of the golden goal : data forecasting.

No matter the language used, many libraries have been and are still published to support such investigations. Often libraries are released aside with their published research papers or use cases are investigated and related by reaserchers into web blogs. A current trend for such data analysis blogs is to reference a Jupyter notebook to illustrate the purpose of the research or the article. This enables a peer validation and allows reusability for the reader.

"_But what if we want to experiment these methodologies on our own dataset ?_"

"_What if we want to combinate multiple data transformations into a complex data pipeline ?_"

"_What if we need to search for the right approach applicable to our data context ?_"

This is **Sen-no-sen**'s purposes:
- for the users : to offer a data analysis experimentation playground with many tools that can be easily combined into advanced analysis recipes
- for the researchers : to give the possibilty to publish or demo their algorithm as ready-to-go analysis block
- for education : to propose a framework to learn data analysis with hands-on aside with theoritical background thanks to the contextual documentation

## Quick Start
1. Click on the vertical tabs to hide/show the panes:
    - the toolbox : this is where the tools are sorted. Pick a tool and drop it on the analysis pane
    - the analysis : the analysis recipe is displayed as nested building blocks (tools)
    - to access to the documentation pane on the right : to get some help and theoritical background on the tool (to come)

2. Click on any tool to display its help file in the documentation pane.
3. Drop any tool on the analysis pane and build your analysis recipe/pipeline
4. Hit 'Generate' to display the result

## Recipe rules
A recipe is built by laying down blocks/tools in a particular configuration. When a tool is dropped onto another one a hierarchical tree is built. The nested tool becomes the child of the previous and inherits of its parent context. The context consists of every data and parameters set by its parent tool. Hence a complete analysis recipe is seen as successive operations performed by the children tools on its parent context.

Tools are grouped by family (datasources, extract, transform, view, analyze, detection, forecast, etc.) and some rules are enforced to guarantee a coherent recipe structure. As an example, datasource may only be dropped as the first tool. In turn, extractors tools are always defined as children of a datasource where they get their data from.
When bulding the recipe, the mouse cursor  guides you with the rules by disabling you to drop the tool on an inapropriate parent.

A typical recipe for an analysis starts from the configuration of a datasource as a provider for the data. On the provider an extractor tool is used to narrow the data of interest by setting the tags to analyse and the time period. The dataset is queried from the parent context.

![](https://github.com/H202Woo/sennosen/blob/main/img/Silverkite%20forecasting%201.jpg "")

## Tools
Tools are organized in groups that make a toolbox. 
Current groups are:
- **Datasources** : to connect to the raw data (configured datasets only for the demo)
    - from databases
    - from preloaded datasets
    - from uploaded CSV files
- **Extract** : narrow the data context upon variables (tags) and period of time
    - from a database table
    - from a file
    - from a dataset
- **Transform** : apply a data transformation on the data as a first difference, log transformation, etc.
- **Visualize** : display the data as
    - a datagrid,
    - a histogram (absolute or with its density function)
    - a line chart for the trends
    - a XY-chart for data correlation
    - basic statistics on the dataset
    - a ACF/PACF chart to highlight its cyclical components
- **Analyze** : show information extracted from the dataset
    - show the data signal enveloppe
    - the seasonality components
    - build a n-order regression over the data
    - show its distribution with n-sigma enveloppe
    - calculate and compare against its moving average
    - evaluate its stationarity with ADF/KPSS 
- **Detect** : anomaly detection feature 
    - Matrix Profile Index 
- **Forecast** : forecasts dataset for a given period 
_**(be patient it's a demo server ;-p )**_
    - use the famous Facebook Prophet algorithm
    - apply Linkedin's Silverkite algo
    - automaticaly find the ARIMA parameters with autoARIMA (max order 3)

A future step will allow you to create and publish your own tool depending on your needs or whenever you want to showcase a library/algo.

### <br>

---
**DISCLAIMER** : Sennosen is still in a early stage of concept and development. The purpose of this repo is to share the idea and the current prototype with the hope of getting some feedback. 
- What do you think of Sennosen for fast data experimentations ?
- What would make you want to use it for yourself ?
- In what context would you use it ? As a hobby, for education, for business purposes ? or...
- Any improvement ideas ?

Share your opinion with us by mail on thinkyWoo@gmail.com we would really appreciate and you would support our side-project effort !

---
## <br>

## Why Sen-no-sen ?
Sen-no-sen (先の先); is a term taken from the japanese martial arts. It litteraly translates as "ahead" but is often extended to "initiave". In this context it means "to take the intiative (of the attack) just before the opponent initiates any movement".
During trainings each opponents throw their souls into the perception of every single movement, sign or intention to attack in order to react accordingly. The name sen-no-sen has been selected for this project as it aims to build a playground for forecasting and data timeserie analysis.

# Installation instructions
Show your interest and I'll make it public ;-)

# Next steps
[ ] Make it OpenSource

[ ] Tool SDK to add your own tools

[ ] Toolbox management : multi-toolbox and tool upload for users

[ ] More tools upon interest: standard SPC, ML, AI, etc.

[ ] Upgrade UI to any Javascript framework ?

**Do you want to collaborate ?** Join us by dropping an email to mailto:thinkyWoo.gmail.com
