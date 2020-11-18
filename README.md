# Make your model count
## A quickstart guide on developing and deploying your machine learning models

# Tools
	- Python
	- Git
	- TensorFlow, NumPy, Matplotlib, Black, PyTest, H5py

# Structure of the project
## The code for training and inference as a Python installable package
	>> pip install -e mymodel

## Package structure
	- mymodel/
		- data/
			- __init__.py
			- load.py               # Loads raw data from some location and sets it up
			- preprocess.py         # Preprocesses data and writes to /train/test folders
		- models/
			- __init__.py           # Defines different models
			- classifier.py         
			- gan.py                
		- training/                 # Trains different models and saves to /checkpoints
			- __init__.py
			- train_classifier.py
			- train_gan.py
		- inference/                # Predicts results and saves to /predictions
			- __init__.py
			- classify.py
			- generate.py
			- explain.py            # Model explanations/other results e.g., Grad-CAM
		- __init__.py
		- utils.py                  # Utility code
	- tests/						# Tests for different scripts
		- __init__.py
		- test_load.py
		- test_preprocess.py
		- test_models.py
		- test_train.py
		- test_inference.py
	- README.md                     # README file describing the project with references
	- LICENSE.md
	- requirements.txt
	- setup.py                      # setup file to make installable Python package

	- notebooks/                    # Optional directories for notebooks/documentation
	- docs/

## Models, data and results (can be located anywhere you want)
	- data/
		- raw/                      # Save raw data using `mymodel.data.load`
		- train/					# Preproceess `mymodel.data.preprocess`
		- test/
	- results
		- predictions/              # Predictions for tasks e.g., computing confusion mat
		- checkpoints/              # Saved checkpoints for models



