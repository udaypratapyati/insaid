![](https://github.com/udaypratapyati/insaid/blob/master/GCD/Projects/GenderRecognitionByVoiceAndSpeechAnalysis/banner.jpeg)

## Gender Recognition by Voice and Speech Analysis

Gender Recognition by Voice and Speech Analysis

This project trains a computer program to identify a voice as male or female, based upon acoustic properties of the voice and speech. The model is trained on a dataset consisting of 3,168 recorded voice samples, collected from male and female speakers. The voice samples are pre-processed by acoustic analysis in R and then processed with artificial intelligence/machine learning algorithms to learn gender-specific traits for classifying the voice as male or female.

The best model achieves an accuracy of 98% on the training set and 98% on the test set.

## Dataset

Download the pre-processed [dataset](https://raw.githubusercontent.com/insaid2018/Term-3/master/Projects/gender_recognition_by_voice.csv) as a CSV file.

The CSV file contains the following fields:

"meanfreq","sd","median","Q25","Q75","IQR","skew","kurt","sp.ent","sfm","mode","centroid","meanfun","minfun","maxfun","meandom","mindom","maxdom","dfrange","modindx","label"

"label" corresponds to the gender classification of the sample. 

In addition to the pre-processed dataset, the raw voice samples used for training are included as .WAV files in a separate repository. The .WAV files are pre-processed in R to produce the above dataset.

## Accuracy
The trained models have achieved the following accuracies (train/test):

### Baseline Algorithm (always male)
50%/50%

### Baseline Algorithm (simple frequency threshold)
57%/57%

### Logistic Regression
97%/97%

### Decision Tree
100%/92%

### Random Forest
99%/94%

### Gradient Boost Classifier
99%/96%

### MLP Classifier (Neural Network)
98%/97%

### Support Vector Classifier
98%/98%

## Acoustic Properties Measured
The following acoustic properties of each voice are measured:

- duration: length of signal
- meanfreq: mean frequency (in kHz)
- sd: standard deviation of frequency
- median: median frequency (in kHz)
- Q25: first quantile (in kHz)
- Q75: third quantile (in kHz)
- IQR: interquantile range (in kHz)
- skew: skewness (see note in specprop description)
- kurt: kurtosis (see note in specprop description)
- sp.ent: spectral entropy
- sfm: spectral flatness
- mode: mode frequency
- centroid: frequency centroid (see specprop)
- peakf: peak frequency (frequency with highest energy)
- meanfun: average of fundamental frequency measured across acoustic signal
- minfun: minimum fundamental frequency measured across acoustic signal
- maxfun: maximum fundamental frequency measured across acoustic signal
- meandom: average of dominant frequency measured across acoustic signal
- mindom: minimum of dominant frequency measured across acoustic signal
- maxdom: maximum of dominant frequency measured across acoustic signal
- dfrange: range of dominant frequency measured across acoustic signal
- modindx: modulation index. Calculated as the accumulated absolute difference between adjacent measurements of fundamental frequencies divided by the frequency range
