To correctly run the code, you need to import the environment from the `environment.yml` file using Anaconda:

`conda env create -f environment.yml`
`conda activate audio`

Files with names ending in `_clean` were used for data preprocessing, and their results are located in the `/data` folder. To save space, the original data has been removed. To run the `_clean` files, you must first download the data from the sources indicated in the bibliography of this engineering thesis.

The model files (`_svm`, `_cnn_mfcc`, and `_cnn_mel_spectrogram`) were originally used to train the models and save them to the `models/` folder. They have now been modified to only test the previously saved models.
