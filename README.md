# DSToolKit
**Plain and simple, this package should make it easy to take a dataset, explore it with some precoded methods, and provide you all that is needed to properly label and store findings.** 

Using this package should ideally facilitate a good habit of adding as much context into a task/project through the use of a well defined `Dataset` and means to explore it and get utility out of it. It's a way for me to automate some of the stuff thats common in most data science tasks with a more tuned eye on reporting and tracking efforts while exploring.

## Dataset
This is an ideally complete dataset that has already gone through any joins and transformations. To kind of enforce this, it requires a csv in its initializer so that it encourages a workflow where final datasets are saved. Also in its initializer is a data dictionary. Again, this is to encourage a good workflow of establishing well defined datasets. A warning will be passed if none is provided and a barebones data dict with default assumptions will be used. ‘Dataset’ is the foundation for ‘Vis’ and ‘Mod’.

## Viz
Methods to create interactive visualizations.

## Mod
Automations for the modeling process.
