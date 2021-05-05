# Improving Daily CT Quality Control By Identifying Ring Artifacts Using Convolutional Neural Networks: A Proof-ofConcept Simulation Study

## Authors
M. N. Fadhel1, A. RAHIMNEJAD YAZDI2, A. A. Mustafa1, I. H. Bercha1;
1Yale New Haven Hospital, New Haven, CT, 2Ryerson University, Toronto, ON, CANADA

## A. RAHIMNEJAD YAZDI Contributions:
Selecting the CNN architecture, applying the model on the images and tunning the hyperparameters : CT_artifacts_final.ipynb


## Summary

### Purpose
Identifying artifacts in CT phantom images is one of the daily quality control (QC) tasks performed by CT technologists. CT scanners are prone to detector miss-calibrations that result in generation of ring artifacts. Identifying this type of artifact is crucial to avoid repeat exams or potential miss-diagnosis. Given the relatively higher doses associated with CT, this becomes particularly important in pediatric imaging. Due to the random occurrence of ring artifacts of varying magnitude, differing technologist subjectivity & the time constraints associated with the daily QC tasks, image artifacts may be missed. The goal of this project was to create a neural network (NN) model that may be able to identify ring artifacts allowing more robust detection of scanner anomalies, independent of factors discussed.

### Methods and Materials
10,000 images of a 32 cm diameter CT uniformity phantom were simulated using Matlab. Half of the simulated images contain three ring artifacts randomly distributed in each phantom image with thicknesses randomly varying between 0.2 cm and 1.0 cm. The ring artifacts were implemented in the sinogram domain for 360 radial projections. The artifactual CT images were computed by filtered back-projection reconstruction technique. Both types of images were randomly displayed and examined just before feeding them in to the convolutional neural network (CNN). A CNN with four convolutional layers followed by a dense layer were trained using Keras in Python with 75% of the images and tested using the rest of the data set. CNN was trained using the RMSProp optimizer. Binary cross entropy loss function was used given the two class classification problem. In the output layer, sigmoid squashing function was employed that maps any predicted value between 0 and 1. We arrived at the employed learning rate based on the accuracy results of the CNN.

### Results
An optimal learning rate of 0.0001 was arrived at, by repeat trials of the CNN. The results demonstrate a highly reproducible CNN model with an accuracy of more than 99.9% & a loss of 0.3 within 10 epochs.
