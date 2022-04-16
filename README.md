# BINARY CLASSIFICATION
## Aim:
To write a python program to perform binary classification.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## Related theoritical concepts
Binary classification refers to predicting one of two classes and multi-class classification involves predicting one of more than two classes. Binary classification is the task of classifying the elements of a set into two groups on the basis of a classification rule.



## Algorithm
1. Define dataset
2. Summarize dataset shape
3. Summarize observations by class label
4. Summarize first few examples
5. Plot the dataset and color the by class label

## Program:

Program to implement binary classification.
Developed by: PRIYADARSHINI R 
RegisterNumber: 212220230038

```
from numpy import where
from collections import Counter
from sklearn.datasets import make_blobs
from matplotlib import pyplot

X,y = make_blobs(n_samples=10,centers=2,random_state=1)
print(X.shape,y.shape)
counter=Counter(y)
print(counter)

for i in range(5):
    print(X[i],y[i])
    
for label, _ in counter.items():
    row_ix=where(y==label)[0]
    pyplot.scatter(X[row_ix,0], X[row_ix,1], label=str(label))
pyplot.legend()
pyplot.show()

```

## Output:

![image](https://user-images.githubusercontent.com/81132849/163678558-1179333c-9a32-4c41-8829-7866aa695df5.png)
![image](https://user-images.githubusercontent.com/81132849/163678588-d8af7d5c-11ff-4360-8b10-555f049db280.png)



## Result:
Thus the python program performed binary classification successfully.
