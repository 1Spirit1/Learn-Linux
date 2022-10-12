# How to install PyCharm on Ubuntu 20.04 Linux Desktop

PyCharm is a graphical IDE (integrated development environment) that can be installed on Ubuntu Desktop. Many 
Python programmers enjoy using PyCharm because it can be used to analyze code, debug programs, and is integrated with 
Git and other version control systems, as well as web development applications. In this tutorial, you will see how to install
PyCharm on Ubuntu 20.04 Focal Fossa Linux.

PyCharm is developed by JetBrains. It is free and open source, or at least the community edition is. Follow along with the steps 
below if you’d like to try PyCharm on Ubuntu for your Python programming needs.

## Software Requirements and Conventions Used

![image](https://user-images.githubusercontent.com/91078843/195446702-ada08386-1975-4275-b155-686034ec8ed0.png)


## Install PyCharm on Ubuntu from command line

> Open termianl by pressing keys:     ctrl + alt + t

#### STEP 1 - Start by opening a terminal window and execution of the bellow apt command. Select your preferred version to install:

```
sudo snap install pycharm-community --classic
```
or
```
sudo snap install pycharm-professional --classic
```
or
```
sudo snap install pycharm-educational --classic
```

#### STEP 2 - Setting up Pycharm on Linux

You can launch it from the start menu or by typing "Pycharm" in the terminal.

When you start up PyCharm for the first time, you will be prompted with terms and conditions.
After accepting the Terms and Conditions, PyCharm will ask you whether you want to send “Anonymous Statistics” or not.


![image](https://user-images.githubusercontent.com/91078843/195448242-edec5629-faa5-4c44-a55e-20e2f4b5bb78.png)


After accepting the necessary terms, you can start your first project in Pycharm or you can open an already existing project.
Other than this you can also open a project from VCS such as Git.

![image](https://user-images.githubusercontent.com/91078843/195448427-f16fd3c4-8c6a-4757-b1bd-d9c09c5b57a6.png)

## Start a New Project : 

1. If you’re on the Welcome screen, click New Project. If you’ve already got any project open, choose File | New Project from the main menu.

2. Although you can create projects of various types in PyCharm, in this tutorial let's create a simple Pure Python project.
   This template will create an empty project.
   
   ![image](https://user-images.githubusercontent.com/91078843/195448762-9f0aaa3a-6fc4-4711-aaf4-e5f81d3fdd9a.png)

3. Choose the project location. Click the Browse button button next to the Location field and specify the directory for your project.
4. Also, deselect the Create a main.py welcome script checkbox because you will create a new Python file for this tutorial.
5. Python best practice is to create a virtualenv for each project. In most cases, PyCharm create a new virtual environment automatically 
   and you don't need to configure anything. Still, you can preview and modify the venv options. Expand the Python Interpreter: New Virtualenv 
   Environment node and select a tool used to create a new virtual environment. Let's choose Virtualenv tool, and specify the location of the environment
   and the base Python interpreter used for the new virtual environment.

   When configuring the base interpreter, you need to specify the path to the Python executable. If PyCharm detects no Python on your machine, it provides
   the following options:
   
      > Specify a path to the Python executable (in case of non-standard installation)

      > Download and install the latest Python versions from python.org

      > Install Python using the Command-Line Developer Tools (macOS only).

![image](https://user-images.githubusercontent.com/91078843/195449137-da30866c-fa72-4f72-909c-583a3e0d5126.png)


## Create a Python File:

1. In the Project tool window, select the project root (typically, it is the root node in the project tree), right-click it, and select File | New ...

![image](https://user-images.githubusercontent.com/91078843/195449273-e1cab90b-0831-4d85-b448-062dd9e5e59e.png)

2. Select the option Python File from the context menu, and then type the new filename.

![image](https://user-images.githubusercontent.com/91078843/195449340-0cd22ca2-32e0-480e-aff3-aff44bf5f50b.png)

3. PyCharm creates a new Python file and opens it for editing.














