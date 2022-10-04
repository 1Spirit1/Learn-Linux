# Steps to Install VS Code in Ubuntu


## Introduction

Microsoft's Visual Studio Code (vscode) is a source-code editor developed for Windows, Linux, and macOS.
The code editor supports debugging, syntax highlighting, automatic code completion, snippets, embedded Git control, etc.

vscode is open source. It supports an abundance of extensions acts as a version control system,
thus facilitating project collaboration.

## Prerequisites

    1) A system running Ubuntu.
    2) An account with administrator privileges.
    3) A working network connection.

## There are two methods to install VS Code:

### Method 1: Install Visual Studio Code with Snap

Snap packages are containerized applications. Open the terminal and run the following command 
to install the vscode self-contained snap package with the required dependencies:

> sudo snap install --classic code

![image](https://user-images.githubusercontent.com/91078843/193876994-b90de9ec-e0d8-499c-abe6-e1a66e3cf2a3.png)

Verify the installation by checking the program version:

> code --version

![image](https://user-images.githubusercontent.com/91078843/193877197-97b5b3a4-8c23-43ab-9578-53fad7d93050.png)


### Method 2: Install Visual Studio Code with apt

#### Step 1: Update the system repository

Run the following command to update the system's repository and ensure you get the latest vscode version:

> sudo apt update

#### Step 2: Install Package Dependencies

For proper operation, vscode requires you to install package dependencies. Run the following
command to resolve package dependencies:

> sudo apt install software-properties-common apt-transport-https wget -y

![image](https://user-images.githubusercontent.com/91078843/193877819-ebb11627-9405-43b4-b192-878f01dfd39a.png)

The command automatically installs any vscode dependencies.
