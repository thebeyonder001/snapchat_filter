# snapchat_filter

In this project we aim to implement the snapchat like filters (in our case we use the glasses filter to experiment) based on the facial keypoints. We use python library OpenCV  and keras for this purpose.
The project is in two parts:
1. Detection of facial keypoints using a model we train from scratch using keras
2. Overlaying the filter according to the facial keypoints predicted by our model
 ## 1. Facial Keypoint Detection
We use keras to train a model from scratch.
We could also use facenet model to improve the accuracy of the model but training a model from scratch gave us the edge of training a smaller and faster model although task-specific.
Data used : https://www.kaggle.com/c/facial-keypoints-detection/data
Trained model : https://drive.google.com/file/d/1qvnIvTNvPR-XWebuExnzrVX3uf2c9Jay/view?usp=sharing
Using image augmentation techniques the performance can be improved and trained beyond the 80% accuracy that i achieved.

## 2. Filter Overlaying
We use opencv haarcascade to detect the face and then resize the image accodingly for our model. Then using the predicted facial keypoints, we overlay the filter
