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
The architecture of the model and number of nodes of each layer was shown as figure below.The model consists of one input layer,two hidden layers where each hidden layer consists of rectified linear activation function,one dropout layer and one output layers with softmax function.
![Architecture of the Model](https://user-images.githubusercontent.com/109932205/181147681-4806872a-c84d-4371-bb00-2be96fbe3779.png)


The model was trained with a batch size of 64 and 100 epochs.Early stopping was implemented.Training was stopped at epoch 80 and the best model weights at 70 epoch was restored.The loss and accuracy parameter of the best model weights was shown at the table below.Besides,the figure below show the graph of training process.

|             | Training | Validation |
| ----------- | -------- | ---------- |
| Loss        | 0.0707   | 0.0640     |
| Accuracy(%) | 97.49    | 98.05      |

Based on the observation it show that the validation loss is lower than the training.This is due to the dropout layer only implement to the training process.Hence, it affect the training loss.It lead the scenario where the training loss is higher than the validation loss.

Refer to the [Link](https://towardsdatascience.com/what-your-validation-loss-is-lower-than-your-training-loss-this-is-why-5e92e0b1747e#:~:text=Sometimes%20data%20scientists%20come%20across,we%20observe%20higher%20training%20loss.) for more explanation.


![Graph](https://user-images.githubusercontent.com/109932205/181149306-644ef844-2088-4615-ab5a-3f7916ab880f.png)



## 4.Result 
The result of test data was shown at figures below. 

![image1](https://user-images.githubusercontent.com/109932205/181150216-6873f1af-7315-42a8-9e73-760dbc551e6b.png)



Metrics of confusion matrix 

![image2](https://user-images.githubusercontent.com/109932205/181150226-70b13714-a0e6-45f1-aa95-af747e331977.png)

**The model able to achieve 97% classification accuracy for the test dataset**





