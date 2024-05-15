# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
### Step 1 :
1.Import the required packages.
### Step 2 :
2.Import the dataset to operate on.
### Step 3 :
3.Split the dataset.
### Step 4 :
4.Predict the required output.
### Step 5:
5.End the program.

## Program:
```python
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Thrinesh Royal.T
RegisterNumber:  212223230226
*/


import chardet
file='spam.csv'
with open(file, 'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv("spam.csv",encoding='Windows-1252')

data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
```

<br>
<br>


```PYTHON
import chardet
file='spam.csv'
with open(file, 'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
result
```

## Output:
![image](https://github.com/SANTHAN-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/80164014/6deeb026-a996-4dbf-8765-32868d17074b)


```python
import pandas as pd
data=pd.read_csv("spam.csv",encoding='Windows-1252')

data.head()
```

## Output :
![image](https://github.com/SANTHAN-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/80164014/a920d22f-1a08-48c0-9b7b-9249ffdf9c43)

```python
data.info()
```
## Output :
![image](https://github.com/SANTHAN-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/80164014/83982f60-b996-4449-b433-8650fcdc6f26)

```python
data.isnull().sum()
```
## Output :
![image](https://github.com/SANTHAN-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/80164014/0f06a488-40fe-41a2-a0a3-14246f71ea9d)

```python
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
```

## Output :
![image](https://github.com/SANTHAN-2006/Implementation-of-SVM-For-Spam-Mail-Detection/assets/80164014/f32f1ca3-e2a0-4c09-99cf-6be228c2c4d6)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
