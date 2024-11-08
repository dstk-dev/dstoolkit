# DSToolKit
**Plain and simple, this package should make it easy to take a dataset, explore it with some precoded methods, and provide you all that is needed to label and store findings.** 

This package should ideally facilitate the good habit of adding as much context into a task/project through the use of a well defined `Dataset`. This `Dataset` has ways to speed up exploratory data analysis and get utility out of it using the `Viz` and `Mod` extensions. As opposed to dumping a bunch of spaghetti code into a notebook file, you can use this package for structuring analysis and funnel findings into reporting. In a more applied and personal sense, it's a way for me to automate some of the stuff thats common in data science tasks that I've encountered. 

Lastly, this package has like a secondary goal or a background goal of fitting into the intel cycle. This package makes analysis and production a cinch and help you to get some useful information over to decision makers.
![image](https://github.com/user-attachments/assets/3ff16d60-0728-4abd-93d5-e26dbc00d394)


Using this package should facilitates a good habit of adding as much context into a task/project through the use of a well defined `Dataset` and means to explore it and get utility out of it. It's a way for me to automate some of the stuff thats common in most data science tasks with a more tuned eye on reporting and tracking efforts while exploring.

# Tools

### MetaData
This is the backbone of a `DataSet`. Its essentially a data dictionary along with any narratives or descriptions of the data. This package assumes a `Path(csv)` but really this extends to any final dataset. Please use `./scripts/metadata_maker.py` to make a `.json` file that can be used to initialize a `MetaData` object to create a `DataSet`. In a pinch, `DataSet` can make assumption of your data dictionary, but please avoid this when possible.

```
{
    "name": "Name of the dataset, e.g., Demographic Study Dataset",
    "description": "Overview of the dataset",
    "origin_notes": "Where the source data came from eg sensors, survey of people in chicago, sales from shopify pos",
    "previous_handler_notes": "Any information regarding the data touched by last handler. Brief overview on transformations applied, cleaning done, etc, eg data engineering team applied filtering of duplicated data",
    "handler_audit_lineage": "Entities who have moved or potentially modified data eg retail store to corporate to sales to my team. survey lab to researchers to uci ml repo to data science hw to me",
    "next_handler_notes": "Notes about entities possibly using your analysis for actionable information next eg corporate team, product data science team, publishing, etc"
    "collection_date": "Date data was collected or created, e.g., 'YYYY-MM-DD'",
    "update_frequency": "How often the dataset is updated, e.g., daily, weekly, monthly",
    "quality_notes": "Notes on data quality or limitations, e.g., self-reported data biases or missing values",
    "data_storage_notes": "Location where data being analyzed is stored, e.g., BigQuery, UCI ML repo, Google Sheets, local server",
    "ready_to_model_data_file_path": "Path to the final dataset file, e.g., '~/data/processed/demographic_study_final.csv'",
    "findings_path": "Path to any notes, models, reports, or charts being generated from analyzed data, e.g., '~/data/reports/'",
    "data_dictionary": [
        {
            "field_index": "Index of the field on the dataset",
            "raw_name": "Original name of the variable in the raw data, e.g., 'AGE_GROUP_1A'",
            "snake_case_name": "Standardized name for coding, e.g., 'age_group_one_alpha'",
            "display_name": "Human-readable name of the variable, e.g., 'Age Group 1A'",
            "data_type": "Data type of the variable. Only pandas dtyped for now will likely be - 'boolean', 'integer', 'string', 'float', 'category', 'list', 'dict', 'timestamp'",
            "description": "Detailed description of the variable, including its meaning and context, e.g., 'Categorizes age ranges for analysis'",
            "units": "Measurement units if applicable, e.g., 'years', 'kg', 'count'",
            "value_range": "Allowed or expected range of values, e.g., '0-100' or ['Group A', 'Group B', 'Group C'], [True, False]",
            "nullable": "Whether the field can contain null values, e.g., true or false",
            "source": "Source of the variable’s data, e.g., 'survey', 'census report', 'variable created by previous handler', 'From raw data source'",
            "transformation_notes": "Any transformations applied to the variable if applicable, e.g., 'Converted from text categories to numeric codes'",
        }
    ]
}

```

### DataSet
This is an ideally complete dataset that has already gone through any joins and transformations. To kind of enforce this, it requires a `Path(csv)` in its `MetaData` initializer so that it encourages a workflow where final datasets are saved. Also in its initializer is a data dictionary. Again, this is to encourage a good workflow of establishing well defined datasets. A warning will be passed if none is provided and a barebones data dictionary with default assumptions will be used. `DataSet` is the foundation for `Vis` and `Mod`.

### Viz
Methods to create interactive visualizations. Question is to either make `DataSet` return a `Viz` object or make `Viz` a stand alone class that takes in any collection objects and title configs and return a `Plotly::Figure`? 

### Mod
Automations for the modeling process.

