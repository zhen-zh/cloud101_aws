---
title: "AWS Elastic Beanstalk"
teaching: 10
exercises: 45
questions:
- "Can we break up the lesson into multiple parts?"
objectives:
- "See that you can have more than one part for the lesson"
keypoints:
- "We can add parts to the lesson, by adding more markdown files"
- "You get the picture"
---
## Prerequisites
- Please have anaconda or a working version of python installed 
- We will be using PyCharm to deploy our Django web framework. Please make sure you have PyCharm installed. 
- The web API code is available here: http://github.com/cloudmaven/web_api

## Deploying an Elastic Beanstalk App

1. Start PyCharm 

2. Create a python environment for your app. You can Use the "terminal" tab at the bottom of your PyCharm app or use the regular terminal. Here I am using conda to create my environment

```
conda create -n env_name python
```

![](/images/01-elasticbeanstalk-0001.png)

3. You are now ready to create your new project. From the File menu, select New Project then Django. Fill in the location where you want to save your project (Here I am saving it to /Users/Amanda/PycharmProjects/beanstalkdemo). Then choose your interepreter. Click the little button on the right of the Interpreter text box, select "Add local" then find the virtual environment that you created earlier. If you created your environment using conda, it should be in your home directory under anaconda. For example, my virtual environment will be stored in ~/anaconda/envs/aws-env/. You will want to add the Python interpreter created in that virtual environment. Here, I am using Python 3.6.0. Click create

![](/images/01-elasticbeanstalk-0002.png)

4. 

5. New Project > Django 

Requirements.txt
appdirs==1.4.3
Django==1.10
packaging==16.8
pyparsing==2.2.0
six==1.10.0

.ebextensions
django.config
option_settings:
  aws:elasticbeanstalk:container:python:
    WSGIPath: blahtest/wsgi.py
