## Automatic Child Speech Recognition Research

##### Purdue University Research | Deep Learning Lead
**Business Problem:** Currently, no such system exists and current speech recognition systems are only about 20% accurate with transcribing young children’s speech.

**Solution Highlights:** 
  * Key leader and contributor in all phases of project life-cycle including data preprocessing, augmentation, feature selection, modeling, validation, and inference.
  * Identified and implemented methods like noise reduction, filter transformations, spectrograms, Mel-Frequency Cepstral Coefficient features, and more in order to build out signal processing infrastructure.  
  * Led Deep Learning team of 4 researchers and built a Deep Convolutional-LSTM Model with Tensorflow achieving a phonetic accuracy of 87%. 

**Write-up:** 

Over the course of this research, I constructed the entire Preprocessing and Feature Extraction pipelines. I also served as the head of the Deep Learning team in which I led 3 other students.

Below is a high-level diagram of our Model Architecture.

<img src="images/sr_diagram.jpg?raw=true" width="550" height="400" />


Our preprocessing pipeline consists of two main phases. The first is a noise reduction algorithm is applied to the audio signal. This helps to remove excess noise through spectral gating.

The next big step of preprocessing is applying a pre-emphasis filter to the audio signal. Pre-emphasis filters help by balancing the frequency spectrum, avoids errors during fourier transforms, and can improve the signal to noise ratio.

Below are 2 graphs. The first shows the original audio signal and the second graph shows the audio signal after going through the preprocessing pipeline:

<img src="images/sr_preproc.png?raw=true" width="550" height="300" />


After the audio signal has been preprocessed we are able to split the signal and transcript in tandem based on previously obtained alignment times. For this system, we are using a phonetic based model. Once each phonetic is split into the respective audio signal time segments, we can derive the Mel Frequency Cepstral Coefficients (MFCC). This can be done with the following steps:

<img src="images/sr_mfcc.png?raw=true" width="550" height="300" />

These MFCC features will be used as the input for our Deep Learning Model.

The architecture of the Deep Learning Model is a Convolutional-LSTM Network. The model will start with several convolutional layers which work to identify relationships between the spacial audio features. The output of the Convolutional layers are passed to a bidirectional LSTM layer which focuses on patterns in the sequences of features.

Currently our models Phonetic test accuracy is at 87.56%. 

###### All Intellectual Property of this work belongs to Purdue University and therefore I cannot show any code.


