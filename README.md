# sleep-stage-classifier
Classifier to identify sleep stages from muscle activity and brain wave data

## Goal
Train a model to **classify** sleep data obtained from mice (*Mus musculus*) into wake, NREM sleep and REM sleep epochs. Features are derived from continuous time series muscle activty in the electromoyogram (EMG) and brain wave activity in the electroencephalogram (EEG). Manual classification of mouse sleep by expert human sleep scorers is a labor-intensive process. Developing a model to accurately and automatically classify stages of sleep from mouse EEG and EMG recordings has the potential to save sleep scientists a lot of time!

## Process
1. The script takes as its input a **version 7 .mat** file containing the features, their associated class, and time information that has been exported from Spike2 acquisition software. See **example.mat** for an example file.

2. The script carries out the following steps:
    - loads data and constructs a feature matrix form the raw features and class dictionaries
    - attempts to classify each epoch using a support vector machine classifer (SVC) model
    - tunes the hyperparameters of the SVC
    - engineers additional features with which to fit an SVC model

 ## Requirements
 - use Python 3
 - required libraries listed in requirements.txt
