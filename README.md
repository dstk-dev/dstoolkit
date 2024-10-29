# DSToolKit
**Plain and simple, this package should make it easy to take a dataset, explore it with some precoded methods, and provide you all that is needed to label and store findings.** 

This package should ideally facilitate the good habit of adding as much context into a task/project through the use of a well defined `Dataset`. This `Dataset` has ways to speed up exploratory data analysis and get utility out of it using the `Viz` and `Mod` extensions. As opposed to dumping a bunch of spaghetti code into a notebook file, you can use this package for structuring analysis and funnel findings into reporting. In a more applied and personal sense, it's a way for me to automate some of the stuff thats common in data science tasks that I've encountered. Lastly, this package has like a secondary goal or a background goal of fitting into the intel cycle. This package makes analysis and production a cinch and help you to get some useful information over to decision makers.
![image](https://github.com/user-attachments/assets/3ff16d60-0728-4abd-93d5-e26dbc00d394)


Using this package should facilitates a good habit of adding as much context into a task/project through the use of a well defined `Dataset` and means to explore it and get utility out of it. It's a way for me to automate some of the stuff thats common in most data science tasks with a more tuned eye on reporting and tracking efforts while exploring.

# Tools

### MetaData
This is the backbone of a `DataSet`. Its essentially a data dictionary along with any narratives or descriptions of the data. This package assumes a `Path(csv)` but really this extends to any final dataset. Please use `./scripts/metadata_maker.py` to make a `.json` file that can be used to initialize a `MetaData` object to create a `DataSet`. In a pinch, `DataSet` can make assumption of your data dictionary, but please avoid this when possible.

### DataSet
This is an ideally complete dataset that has already gone through any joins and transformations. To kind of enforce this, it requires a `Path(csv)` in its `MetaData` initializer so that it encourages a workflow where final datasets are saved. Also in its initializer is a data dictionary. Again, this is to encourage a good workflow of establishing well defined datasets. A warning will be passed if none is provided and a barebones data dictionary with default assumptions will be used. `DataSet` is the foundation for `Vis` and `Mod`.

### Viz
Methods to create interactive visualizations. Question is to either make `DataSet` return a `Viz` object or make `Viz` a stand alone class that takes in any collection objects and title configs and return a `Plotly::Figure`? 

### Mod
Automations for the modeling process.

