# Music_Genre_Classification

We will try to model a classifier to classify songs into different genres. Let us assume a scenario in which, for some reason, we find a bunch of randomly named MP3 files on our hard disk, which are assumed to contain music. Our task is to sort them according to the music genre into different folders such as jazz, classical, country, pop, rock, and metal.

We will be using the famous GITZAN dataset for our case study. This dataset was used for the well-known paper in genre classification “ Musical genre classification of audio signals “ by G. Tzanetakis and P. Cook in IEEE Transactions on Audio and Speech Processing 2002.
#### Link: https://www.kaggle.com/lnicalo/gtzan-musicspeech-collection

The dataset consists of 1000 audio tracks each 30 seconds long. It contains 10 genres namely, blues, classical, country, disco, hiphop, jazz, reggae, rock, metal and pop. Each genre consists of 100 sound clips.

## Preprocessing the Data
Before training the classification model, we have to transform raw data from audio samples into more meaningful representations. The audio clips need to be converted from .au format to .wav format to make it compatible with python’s wave module for reading audio files. I used the open source SoX module for the conversion. Here is a handy cheat sheet for SoX conversion.

### sox input: .au, output: .wav

## Classification

### Feature Extraction
We then need to extract meaningful features from audio files. To classify our audio clips, we will choose 5 features, i.e. Mel-Frequency Cepstral Coefficients, Spectral Centroid, Zero Crossing Rate, Chroma Frequencies, Spectral Roll-off. All the features are then appended into a .csv file so that classification algorithms can be used.

### Classification
Once the features have been extracted, we can use existing classification algorithms to classify the songs into different genres. You can either use the spectrogram images directly for classification or can extract the features and use the classification models on them.

The processed audio files are stored in 'data.csv' file.
