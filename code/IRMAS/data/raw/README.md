# IRMAS Raw Audio

This folder should contain the IRMAS training audio files organized by instrument class.

Place the subfolders extracted from `IRMAS-TrainingData.zip` here before running `code/IRMAS/notebooks/preprocessing/clean.ipynb` and `code/IRMAS/notebooks/preprocessing/feature_extraction.ipynb`.

The preprocessing notebooks will generate extracted features in `code/IRMAS/features/`.

The machine learning notebooks in `code/IRMAS/notebooks/machine_learning/` are configured for evaluation by default and can use saved models from `code/IRMAS/models/`.

The subfolder structure looks like this:

- `cel/` — cello
- `cla/` — clarinet
- `flu/` — flute
- `gac/` — acoustic guitar
- `gel/` — electric guitar
- `org/` — organ
- `pia/` — piano
- `sax/` — saxophone
- `tru/` — trumpet
- `vio/` — violin
- `voi/` — voice

Download the dataset from:

- https://www.upf.edu/web/mtg/irmas
