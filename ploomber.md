```
pip install ploomber
ploomber examples -n templates/ml-basic
```

Updated the pipeline.yaml file to just run a notebook.

Needed to a `products` and `upstream` to the notebooks and get the pipeline.yaml
fixed up.

Ran `ploomber install --create-env` to create a environment