Understanding Workloads in OpenShift
==============================
_Efficiently fingerprint workloads running in OpenShift clusters in order to make better business decision and offer customer insights into security, reliability, or maintainability issues._

As part of the remote health monitoring, the workloads running on OpenShift clusters are of interest to the business, to the product roadmap, to the engineering organization, and to the customer success organization. Workload fingerprinting refers to taking a number of snapshots of operational and performance metrics related to workloads deployed in clusters, and then aggregating and classifying them to create a 'signature' or 'fingerprint' of the workload. This kind of analysis can help us understand customer usage patterns, identify problematic workloads, make performance tuning decisions, etc.

This project aims to do an EDA of different workloads based on the insight archive data, and then use ML for identifying and analysing the types (i.e. clusters) of workloads that customer run.

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── Pipfile            <- Pipfile stating package configuration as used by Pipenv.
    ├── Pipfile.lock       <- Pipfile.lock stating a pinned down software stack with as used by Pipenv.
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file stating direct dependencies if a library
    │                         is developed.
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    ├── .thoth.yaml        <- Thoth's configuration file
    ├── .aicoe-ci.yaml     <- AICoE CI configuration file (https://github.com/AICoE/aicoe-ci)
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
