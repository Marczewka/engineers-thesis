Aby poprawnie uruchomić kod, należy zaimportować środowisko z pliku environment.yml za pomocą Anaconda:
conda env create -f environment.yml
conda activate audio

Pliki z nazwą kończącą się na _clean służyły do wstępnego przetwarzania danych, a ich wyniki znajdują się w folderze /data. 
W celu oszczędności miejsca oryginalne dane zostały usunięte. Aby uruchomić pliki _clean, należy uprzednio pobrać dane ze 
źródeł wskazanych w bibliografii niniejszej pracy inżynierskiej.

Pliki modeli (_svm, _cnn_mfcc oraz _cnn_mel_spectrogram) zostały pierwotnie wykorzystane do trenowania modeli oraz zapisania 
ich do folderu models/. Obecnie zostały zmodyfikowane tak, aby jedynie testować zapisane wcześniej modele.
