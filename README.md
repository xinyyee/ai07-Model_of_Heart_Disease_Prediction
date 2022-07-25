# ai07 Heart Disease Prediction Using Feedforward Neural Network

## 1.Objective
The objective of this project is to create a model of feedforward neural network to predict the presence of heart disease in the patient(Classification Problem).The model is trained with [Heart Disease Dataset](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset).

Refer to the link above for more details about the data.

## 2.IDE and Framework
Jupyter notebook is the main IDE.The main framework used in this project are Pandas,Scikit-learn and Tensorflow Keras.


## 3.Methodology
### 3.1 Data Pipeline
There is no unwanted features required to be removed.Next, the dataset was splitted into train-validation-test sets with a ratio of 70:20:10.

### 3.2 Model Pipeline 
The architecture of the model and number of nodes of each layer was shown as figure below.The model consists of one input layer,three hidden layers where each hidden layer consists of rectified linear activation function and one output layers with softmax function.
![Architecture of the Model](https://user-images.githubusercontent.com/109932205/180715267-ea0290f9-aa73-4902-a5cd-4665798e73f4.png)


The model was trained with a batch size of 64 and 100 epochs.Early stopping was implemented.Training was stopped at epoch 31 with loss and accuracy parameter was shown at the table below.Besides,the figure below show the graph of training process.

|             | Training     | Validation    |
| :---        |    :----:    |          ---: |
| Loss        |   0.0624     |    0.0741     |
| Accuracy(%) | 98.6         |   98.1        |



![Graph](https://user-images.githubusercontent.com/109932205/180720007-6a32aa7d-9e53-4a77-b997-910784322462.png)


## 4.Result 
The result of test data was shown at figures below. 

![Evaluation score](https://user-images.githubusercontent.com/109932205/180721033-54b29928-54af-4f8e-86b3-f75fd412806e.png)

Metrics of confusion matrix 

![Confusion Matrix](https://user-images.githubusercontent.com/109932205/180721220-e579cbd1-44ab-4b13-89cd-3ad6d61846f4.png)

**The training result can improve by adding more layers and increasing the number of epoch.**





