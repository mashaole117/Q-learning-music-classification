# Q-learning-music-classification

This project makes use of the GTZAN dataset to build classifiers for pieces of music into genres. The classifier with the highest accuracy is used to initilaize a Q-table used in the implementation of a Q-learing reinforcement algorithm.

## Results
The evaluation metric used for the four classifiers was a confusion matrix which allowed for the calculation of the accuracy score in classification. The Support Vector Machine achieved the highest accuracy score of 75.5%. Using the predictions made by the SVM model on testing data in the GTZAN, the Q table was initialized with +0.01 for positive label predictions and -0.01 for negative label predictions. The system then requests a song related to a specified genre. If the song fits in the genre, a reward of +1 is given to the algorithm, if not a 1 is given instead.

## Requirements
scikit-learn <br />
pandas <br />
matplotlib <br />
seaborn <br />

