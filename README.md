# Facial-Analysis-App-
Django Web app for facial and emotional recognition using OpenCV pretrained resnet-10 caffe model that uses single shot multibox detector (SSD) framework for face and emotion detection. 

## Methodology:

### Data Preprocessing
1) Used pretrained resnet-10 for facial recognition of different public figures
2) Facial/Emotional feature extraction/embedding as vectors 
3) Vectorized features and labels saved in a hash table as a pkl file to train models

### Model Training 
1) Trained voting classifier with adjusted weights based on individual model performance using a random forest, SVM, logistic regression on compiled labeled vectors
2) Pipelining facial recognition and emotional recognition models to be used in django web app 


## Notable Findings:
1)SVM model performed best with an individual f1 score of 71 % 
2) Random Forest was severely overfit 
3) Voting Classifier with SVM, log, random forest models performed best with f1-score of 72% on test set and accuracy score of 70%
4) Emotion recognition models achieved significantly lower f1 (39%) and accuracy score(45) compared to facial recognition models


## Deployment
Django Web App Deployed on Heroku: https://face-recognition-django-app.herokuapp.com/


![Screen Shot 2021-11-17 at 11 19 02 AM](https://user-images.githubusercontent.com/61222734/142267932-83b9eccc-fa9c-4f75-8fd3-845e7f5ffda3.png)
