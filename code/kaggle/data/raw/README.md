# Kaggle Raw Audio

This folder should contain the Kaggle competition `.wav` training files required by the preprocessing notebooks.

Place all extracted training audio files from `FSDKaggle2018.audio_train.zip` directly in this folder before running `code/kaggle/notebooks/preprocessing/clean.ipynb` and `code/kaggle/notebooks/preprocessing/feature_extraction.ipynb`.

The preprocessing notebooks will generate extracted features in `code/kaggle/features/`.

The machine learning notebooks in `code/kaggle/notebooks/machine_learning/` are configured for evaluation by default and can use saved models from `code/kaggle/models/`.

Download the dataset from:

- https://www.kaggle.com/competitions/freesound-audio-tagging/data
