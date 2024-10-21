# DSToolKit
**Plain and simple, this package should make it easy to take a dataset, explore it with some precoded methods, and provide you all that is needed to label and store findings.** 

This package should ideally facilitate the good habit of adding as much context into a task/project through the use of a well defined `Dataset`. This `Dataset` has ways to speed up exploratory data analysis and get utility out of it using the `Viz` and `Mod` extensions. As opposed to dumping a bunch of spaghetti code into a notebook file, you can use this package for structuring analysis and funnel findings into reporting. In a more applied and personal sense, it's a way for me to automate some of the stuff thats common in data science tasks that I've encountered. Lastly, this package has like a secondary goal or a background goal of fitting into the intel cycle. This package makes analysis and production a cinch and help you to get some useful information over to decision makers.
![image](https://github.com/user-attachments/assets/3ff16d60-0728-4abd-93d5-e26dbc00d394)



## Dataset
This is an ideally complete dataset that has already gone through any joins and transformations. To kind of enforce this, it requires a csv in its initializer so that it encourages a workflow where final datasets are saved. Also in its initializer is a data dictionary. Again, this is to encourage a good workflow of establishing well defined datasets. A warning will be passed if none is provided and a barebones data dict with default assumptions will be used. ‘Dataset’ is the foundation for ‘Vis’ and ‘Mod’.

## Viz
Methods to create interactive visualizations.

## Mod
Automations for the modeling process.

