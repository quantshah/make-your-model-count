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
    - mymodel/
      - data/
        - __init__.py
        - load.py          # Loads raw data
        - preprocess.py    # Preprocesses data
      - models/
        - __init__.py      # Defines different models
        - classifier.py         
        - gan.py                
      - training/            # Trains different models
        - __init__.py
        - train_classifier.py
        - train_gan.py
      - inference/           # Predicts results
        - __init__.py
        - classify.py
        - generate.py
        - explain.py       # Model explanations e.g., Grad-CAM
      - utils.py             # Utility code
    - tests/               # Tests
      - __init__.py
      - test_load.py
      - test_preprocess.py
      - test_models.py
      - test_train.py
      - test_inference.py
    - README.md            # Describes the project
    - LICENSE.md
    - requirements.txt
    - setup.py          

    - notebooks/           # Optional directories
    - docs/

## Models, data and results
#### These folders can be in any location where you actually run your project.
    - data/
      - raw/               # Save raw data using `mymodel.data.load`
      - train/             # Preproceess `mymodel.data.preprocess`
      - test/
    - results
      - predictions/       # Predictions for tasks e.g., computing confusion mat
      - checkpoints/       # Saved checkpoints for models
