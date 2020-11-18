# Make your model count
#### A quickstart guide on developing and deploying your machine learning models.

# Tools
    - Python
    - Git
    - TensorFlow, NumPy, Matplotlib, Black, PyTest, H5py

# Structure of the project
#### The code for training and inference as a Python installable package.
    >> pip install -e mymodel

## Package structure
    ├── mymodel
    │   ├── models             # Defines different models
    │   │   ├── __init__.py
    │   │   ├── classifier.py
    │   │   └── gan.py
    │   ├── training           # Trains different models
    │   │   ├── __init__.py
    │   │   ├── train_classifier.py
    │   │   └── train_gan.py
    │   ├── inference
    │   │   ├── __init__.py
    │   │   ├── classify.py
    │   │   ├── explain.py     # Model explanations e.g., Grad-CAM
    │   │   └── generate.py
    │   ├── data
    │   │   ├── __init__.py
    │   │   ├── load.py        # Loads raw data
    │   │   └── preprocess.py  # Preprocesses data
    │   ├── __init__.py
    │   └── utils.py           # Utility code
    ├── tests                  # Tests
    │   ├── __init__.py
    │   ├── test_inference.py
    │   ├── test_load.py
    │   ├── test_models.py
    │   ├── test_preprocess.py
    │   └── test_train.py    
    ├── README.md              # Describes the project
    ├── LICENSE
    ├── requirements.txt
    ├── setup.py
    ├── docs                   # Optional directories
    ├── notebooks    

## Models, data and results
#### These folders can be in any location where you actually run your project.
    ├── data
    │   ├── raw
    │   ├── test
    │   └── train
    └── results
        ├── checkpoints
        └── predictions
