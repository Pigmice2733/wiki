
# Opencv Installation Process 
Here are the steps, that you will **run in a terminal shell** that will get you ready to run the [OpenCV](https://opencv.org/) 
library and vision track!

## For Linux 
Make sure your version of python is up to date 
```
sudo apt-get install python3-pip
```
Install the OpenCV Library
```
sudo apt-get install python-opencv
```
Install pipenv so we can create a virtual enviroment. A virtual enviroment means the libraries we install only happen in that directory, and won't effect code in other "places" or folders of our computer
```
sudo pip3 install pipenv
```
Either manually create a folder or create a folder called vision-tracking-exp or vt-exp (whatever you'd like) through the terminal:
```
mkdir vt-xp ; cd vt-xp
```
Cd into that project 
```
cd vt-exp
```
Create a new project using python version three
```
pipenv install --three
```
Whenever we want a new virtual enviorment for a project we can use this command. If you ever start a new project in a different directory, now all you need to do is this line, because everything else is installed: 
```
pipenv shell
```
