```
pip install ploomber
ploomber examples -n templates/ml-basic
```

Updated the pipeline.yaml file to just run a notebook.

Needed to a `products` and `upstream` to the notebooks and get the pipeline.yaml
fixed up.

Ran `ploomber install --create-env` to create a environment

```
source venv-womens_wc_23/bin/activate
ploomber build
```

Had to fix the parameter tag on the cells in the notebook to get it to run.

Then I had to fix an error with throwing all the predictions in a parquet file