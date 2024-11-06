# Storing Metadate
After doing some research there is no specific package whose focus is to store data dict or metadata info using python. UCI however has a pretty good way that it baked into it python api.

- [Example Notebook on UCI Repo Py Package](https://github.com/uci-ml-repo/ucimlrepo/blob/main/src/demo.ipynb)
    - [`fetch_repo()`](https://github.com/uci-ml-repo/ucimlrepo/blob/66747cb189eddd5fc747c4bf74ed4985a2c17454/src/ucimlrepo/fetch.py#L150) returns a dict that bundles table metadata, raw data, and data dictionary 
    - UCI has an architecture where users (see notebook) look for a datasets metadata first and within that metadata is a url to the actual data. 
    - User fetches dataset [url](https://github.com/uci-ml-repo/ucimlrepo/blob/66747cb189eddd5fc747c4bf74ed4985a2c17454/src/ucimlrepo/fetch.py#L68C43-L68C50) and adds `id=827`. Url gets transformed to this https://archive.ics.uci.edu/api/dataset?id=827. That metadata json return has a `data_url` that has a url to the raw data. metadata info gets split into `metadata` and `variables`. raw data gets set into `data`.
    - Overall, similar to my package, metadata is the entrypoint to working with the data. Im curious to what their onboard for data is like? Like if a researcher wants to have their data posted on the UCI repo what do they need to submit?
    - I like that the metadata url has a ton of stuff and is similar to what I would want to have. I also like that its essentially an api server. I think id like my package to show a usecase for a way to serve data this way. Kind of like a plug and play to set this architecture up for an organization. 
