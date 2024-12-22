# SMUL Group Assignment 3 of Group 4

Authors:

    Bernarndo Vicente 202008545
    Miguel Gouveia    202302221

This is a repository to store the project of Group 4 in Environmental Sound Classification for the SMUL course Group Assignment 3.

## Software Versions

Software Versions used:

[-] Python 3.11.11
[-] msclap 1.3.3
[-] torch 2.1.2
[-] numpy 1.26.4
[-] pandas 2.2.3
[-] tqdm 4.67.1
[-] matplotlib 3.9.4
[-] seaborn 0.13.2

## Dataset and Set Up

For this Environmental Sound Classification assignment, the US8K dataset was used. A compressed file was downloaded from the dataset's website: https://urbansounddataset.weebly.com/urbansound8k.html. The comrpessed file was placed in a folder named 'dataset', in the same directory as the notebooks folder. Uncompressing the file should result in the following structure:

C:.
└───SMUL_GA03_G4_SoundClassification
    ├───dataset
    │   └───UrbanSound8K
    │       ├───audio
    │       │   ├───fold1
    │       │   ├───fold10
    │       │   ├───fold2
    │       │   ├───fold3
    │       │   ├───fold4
    │       │   ├───fold5
    │       │   ├───fold6
    │       │   ├───fold7
    │       │   ├───fold8
    │       │   └───fold9
    │       └───metadata
    └───notebooks

If the following structure is not met, then the path variables used in the notebooks will probably require alteration to match the system's directory strucutre.

All the notebooks use the CLAP model version of 2023.

The notebooks folder contains three jupyter notebooks: zero_shot_prediction, zero_shot_classification and zero_shot_classification_cross_validation.

The zero_shot_prediction notebook takes an audio file from the US8K dataset, takes the labels from the dataset and then makes a prediction of which of the classes best fit the audio. It will show the true label of the file and the percentages of the top picked classes.

The zero_shot_classification notebook takes the whole dataset and it's true labels, makes predictions on the whole dataset and finally determines the model's accuracy along with it's confusion matrix.

The zero_shot_classification_cross_validation notebook works similarly to the zero_shot_classification notebook, except it makes the predictions per fold, and measures the accuracy per folder. The total accuracy of the model is the average accuracy along the 10 folds. This is the 10-fold cross validation method.