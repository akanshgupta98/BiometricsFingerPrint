# BiometricsFingerPrint
This Project consists of 3 parts:
1. Detecting whether the finger print obtained is real or altered.
2. If it is not real, then the type of alteration applied to the fingerprint.
3. Detecting gender from the fingerprint obtained.

Tools Used: Pytorch, Google Colab

## Dataset Used:
LINK: https://www.kaggle.com/ruizgara/socofing
The dataset has been taken from kaggle. Sokoto Coventry Fingerprint Dataset (SOCOFing) is a biometric fingerprint database designed for academic research purposes. 
SOCOFing is made up of 6,000 fingerprint images from 600 African subjects and contains unique attributes such as labels for gender, hand and finger name as well as 
synthetically altered versions with three different levels of alteration for obliteration, central rotation, and z-cut.
The total images of the fingerprints are around 50,000 and all are in BMP format. The size of the dataset is around 800MB.

## Pre-Processing:
Randomized under-sampling and Normalization of the data has been performed according to the given tasks due to imbalanced data.

## Architectures:
Many different architectures were used and experimented. 
The tried models:
1. Inception_v3
2. ALex Net
3. VGG
4. Mobile Net
5. LeNet
6. Custom Model

Only Alex Net gave promising results. Other models were taking a lot of time and generally were overfitting.
Tranfer Learning has been used and only some middle layers of the architecture were trained. 

## Experiment:
An experiment has been done. 2 CNN architectures were made and trained independently, and then concatenated into 1 and then trained further. This experiment
was not able to achieve desired results but gave a good experience working with CNNs. The idea was to promote weight sharing. Unfortunately this approach also was
overfitting and even after tuning many parameters, applying regularization, tweaking some other things also, the approach could not work well for this project.

## Results:
### Real vs Altered :
Train : 99 %
Test : 98 %

### Types of alterations :
Train : 99.4 %
Test : 94.8 % 

### Gender Detection : 
Train : 83.3 %
Test : 83 %

Confusion matrix has been plotted for all. 
