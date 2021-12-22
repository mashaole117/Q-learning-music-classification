# Q-learning-music-classification

This project makes use of the GTZAN dataset to build classifiers for pieces of music into genres. The classifier with the highest accuracy is used to initilaize a Q-table used in the implementation of a Q-learing reinforcement algorithm.

## Results
The evaluation metric used for the four classifiers was a confusion matrix which allowed for the calculation of the accuracy score in classification. The Support Vector Machine achieved the highest accuracy score of 75.5%. Using the predictions made by the SVM model on testing data in the GTZAN, the Q table was initialized with +0.01 for positive label predictions and -0.01 for negative label predictions. The system then requests a song related to a specified genre. If the song fits in the genre, a reward of +1 is given to the algorithm, if not a 1 is given instead. <br />
![SVM_confusion_matrix](https://user-images.githubusercontent.com/93128720/147085157-fc702fdd-09f5-4069-9f04-1046f8ebc00d.png)


The confusion matrix produced by the learned Q-table is similar to that of the SVM. Indicating that the initial biasing of the Q table limited it’s ability to achieve accuracies beyond the SVM’s 75.5%, but merely matched it.<br />
![q_confusion](https://user-images.githubusercontent.com/93128720/147085183-6307e505-2f8c-4826-8824-b0dd3b803b83.png)


## Requirements
scikit-learn <br />
pandas <br />
matplotlib <br />
seaborn <br />

