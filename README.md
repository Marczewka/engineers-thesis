# Automatic Recognition of Musical Instruments in an Audio Recording

## Overview

This repository contains the code, extracted features, saved models, and thesis sources for the thesis project titled "Automatic Recognition of Musical Instruments in an Audio Recording." The implementation covers two datasets:

- `IRMAS` – audio instrument recognition from instrument-labeled recordings
- `kaggle` – Freesound Audio Tagging dataset from a Kaggle competition

The repository includes data preprocessing notebooks, model training notebooks, saved models, extracted feature sets, and the LaTeX source for the engineer's thesis.

The compiled thesis PDF is available here:

- [Grzegorz_Marczewski_praca_inzynierska.pdf](engineers-thesis/Grzegorz_Marczewski_praca_inzynierska.pdf)

## Project Structure

- `environment.yml` – conda environment definition
- `engineers-thesis/` – LaTeX thesis source, support files and final PDF
- `code/IRMAS/` – IRMAS dataset preprocessing, features, models, and notebooks
- `code/kaggle/` – Kaggle dataset preprocessing, features, models, and notebooks

Each dataset folder follows a similar structure:

- `data/raw/` – raw audio files (empty)
- `data/meta/` – metadata files for Kaggle only (empty)
- `data/clean/`, `data/segmented/` – derived dataset versions (empty)
- `features/` – extracted feature arrays `X.npy` and `y.npy` (empty)
- `models/` – trained model files
- `notebooks/` – preprocessing and machine learning notebooks
- `images/` – generated visualizations and example plots (spectrograms, mel-spectrogram images, confusion matrices)
- `histories/` – saved training history logs and artifacts (training/validation loss and metric traces)
- `evaluations/` – saved evaluation outputs and reports (prediction CSVs, evaluation metrics, and plots)

## Setup

Install the Anaconda environment and activate it:

```bash
conda env create -f environment.yml
conda activate audio_thesis
```

## Training Requirements

The machine learning notebooks in `code/*/notebooks/machine_learning/` are configured for evaluation by default: long-running training cells are commented out, and the notebooks can still use saved models from `code/*/models/`.

To retrain the models, you need to:

1. Download the raw data as specified in [Training Data Sources](#training-data-sources).
2. Create preprocessed files using `code/*/notebooks/preprocessing/clean.ipynb`.
3. Extract features using `code/*/notebooks/preprocessing/feature_extraction.ipynb`.
4. Uncomment training sections in the `code/*/notebooks/machine_learning/` notebooks.
5. Run the training cells in the machine learning notebooks.

## Training Data Sources

#### IRMAS

Download IRMAS training data `IRMAS-TrainingData.zip` from:

- https://www.upf.edu/web/mtg/irmas

Then put the training files in `code/IRMAS/data/raw/` using the instrument subfolder layout from the dataset.

#### Kaggle

Download the Kaggle competition training data `FSDKaggle2018.audio_train.zip` and metadata `FSDKaggle2018.meta.zip` from:

- https://www.kaggle.com/competitions/freesound-audio-tagging/data

Put the audio files and metadata files in the following folders:

- `code/kaggle/data/raw/` – all `*.wav` training audio files
- `code/kaggle/data/meta/` – metadata CSV files

## Notebooks

With the raw data from [Training Data Sources](#training-data-sources), use the preprocessing notebooks to generate the extracted feature datasets:

- `code/*/notebooks/preprocessing/clean.ipynb`
- `code/*/notebooks/preprocessing/feature_extraction.ipynb`

Then use the machine learning notebooks for evaluation or training:

- `code/*/notebooks/machine_learning/cnn_melspectrogram.ipynb`
- `code/*/notebooks/machine_learning/cnn_mfcc.ipynb`
- `code/*/notebooks/machine_learning/svm.ipynb`

## Artifacts

- `code/*/features/` — locally generated extracted feature datasets (`X.npy`, `y.npy`). These folders are empty by default in the repository and must be filled by running the preprocessing notebooks.
- `code/*/models/` — trained model files (Keras `.keras` files).
- `code/*/images/` — generated visualizations and example plots (spectrograms, mel-spectrogram images, confusion matrices).
- `code/*/histories/` — saved training history logs and artifacts (training/validation loss and metric traces).
- `code/*/evaluations/` — saved evaluation outputs and reports (prediction CSVs, evaluation metrics, and plots).

The prepopulated artifact folders are included to allow quick evaluation and reproduction of results without re-running expensive preprocessing or training steps. If you want to regenerate features or retrain models, follow the [Training Requirements](#training-requirements).

## Thesis Source

The thesis source, compilation files and final PDF are located in:

- `engineers-thesis/`

The compiled thesis PDF is available here:

- [Grzegorz_Marczewski_praca_inzynierska.pdf](engineers-thesis/Grzegorz_Marczewski_praca_inzynierska.pdf)
