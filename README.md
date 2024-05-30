# Real time chat application

## Description 
This project aims to develop a real-time chat application with video call functionality, a news app with rendering capabilities, and a fake news detection system using Django and machine learning. A Group video calling application using the Agora Web SDK with a Django backend.

##  How to use this source code

- Clone the repository.
- Open CMD in working directory.
- Run `pip install -r requirements.txt`
- Open project in any IDE(Pycharm or VSCode)
- Run chatapp `python manage.py runserver 8000`, go to the `http://127.0.0.1:8000/
- Run videocall app `python manage.py runserver 9000`,  `http://127.0.0.1:5000/
- Run fake news app `Fake_News_Det.py`, `http://127.0.0.1:9000/`
-go to the `http://127.0.0.1:8000/
- You can check web app is working fine. Sometimes predictions may be wrong.


#### 1 - Clone repo
```

```

#### 2 - Install requirements
```
pip install -r requirements.txt
```

#### 3 - Update Agora credentals
In order to use this project you will need to replace the agora credentials in `views.py` and `streams.js`.

Create an account at agora.io and create an `app`. Once you create your app, you will want to copy the `appid` & `appCertificate` to update `views.py` and `streams.js`. If you have questions about where to get your app I'd recommend referencing this link `https://youtu.be/HX6AM_1-jNM?t=88`

###### views.py
```
def getToken(request):
    appId = "YOUR APP ID"
    appCertificate = "YOUR APPS CERTIFICATE"
    ......
```

###### streams.js
```
....
const APP_ID = 'YOUR APP ID'
....
```


#### 4 - Start server
```
python manage.py runserver 8000
python manage.py runserver 9000
```

#### 5 - Run

Fake_News_Det.py

#  Fake News📰 Classification feature using Python

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)                 
[![Python 3.6](https://img.shields.io/badge/python-3.6-blue.svg)](https://www.python.org/downloads/release/python-360/)   


## Note
- This news prediction feature is not working in real time, because model was trained on historic & limited data.
- For real time building of this kind of system, we need updated dataset and we need to build a model in particular interval of time, because news data can be updated in seconds, so our model should be also updated with the data.




*REQUIREMENTS----

agora-token-builder==1.0.0
asgiref==3.4.1
Django==4.0.1
sqlparse==0.4.2
tzdata==2021.5
scikit-learn == 0.22.1
pandas
numpy
Flask
