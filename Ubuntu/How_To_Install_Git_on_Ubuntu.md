# Introduction

Version control systems like Git are essential to modern software development best practices. Versioning allows you to keep track of your software at the source level. You can track changes, revert to previous stages, and the branch to create alternate versions of files and directories.
Many software projects’ files are maintained in Git repositories, and platforms like GitHub, GitLab, and Bitbucket help to facilitate software development project sharing and collaboration.
In this guide, we will go through how to install and configure Git on an Ubuntu 20.04 server. We will cover how to install the software in two different ways: via the built-in package manager, and source. Each of these approaches comes with its benefits depending on your specific needs.

# Prerequisites
You will need an Ubuntu 22.04 server with a non-root superuser account.
To set this up, you can follow our Initial Server Setup Guide for Ubuntu 20.04.
With your server and user set up, you are ready to begin.

# Installing Git with Default Packages
The option of installing with default packages is best if you want to get up and running quickly with Git, if you prefer a widely-used stable version, or if you are not looking for the newest available functionalities. If you are looking for the most recent release, you should jump to the section on installing from source.

Git is likely already installed in your Ubuntu 20.04 server. You can confirm this is the case on your server with the following command:
```bash
git --version
```
If you receive output similar to the following, then Git is already installed.
```bash
Output
git version 2.25.1
```
If this is the case for you, then you can move on to setting up Git, or you can read the next section on how to install from source if you need a more up-to-date version.

However, if you did not get the output of a Git version number, you can install it with the Ubuntu default package manager APT.

First, use the apt package management tools to update your local package index.
```bash
sudo apt update
```
With the update complete, you can install Git:
```bash
sudo apt install git
```
You can confirm that you have installed Git correctly by running the following command and checking that you receive relevant output.
```bash
git --version
```
Output
```bash
git version 2.25.1
```
# Installing Git from Source
If you’re looking for a more flexible method of installing Git, you may want to compile the software from the source, which we will go over in this section. This takes longer and will not be maintained through your package manager, but it will allow you to download the latest release and will give you greater control over the options you include if you wish to make customizations.

Verify the version of Git currently installed on the server:
```bash
git --version
```
If Git is installed, you’ll receive output similar to the following:
Output
```bash
git version 2.25.1
```
Before you begin, you need to install the software that Git depends on. This is all available in the default repositories, so we can update our local package index and then install the relevant packages.

```bash
sudo apt update
sudo apt install libz-dev libssl-dev libcurl4-gnutls-dev libexpat1-dev gettext cmake gcc
```
After you have installed the necessary dependencies, create a temporary directory and move into it. This is where we will download our Git tarball.
```bash
mkdir tmp
cd /tmp
```
From the [Git project website](https://git-scm.com/), we can navigate to the tarball list available at https://mirrors.edge.kernel.org/pub/software/scm/git/ and download the version you would like. At the time of writing, the most recent version is 2.26.2, so we will download that for demonstration purposes. We’ll use curl and output the file we download to git.tar.gz.
```bash
curl -o git.tar.gz https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.26.2.tar.gz
```
Unpack the compressed tarball file:
```bash
tar -zxf git.tar.gz
```
Next, move into the new Git directory:
```bash
cd git-*
```
Now, you can make the package and install it by typing these two commands:
```bash
make prefix=/usr/local all
sudo make prefix=/usr/local install
```
Now, replace the shell process so that the version of Git we just installed will be used:
```bash
exec bash
```
With this complete, you can be sure that your install was successful by checking the version.
```bash
git --version
```
With Git successfully installed, you can now complete your setup.

# Setting Up Git
After you are satisfied with your Git version, you should configure Git so that the generated commit messages you make will contain your correct information and support you as you build your software project.

Configuration can be achieved by using the git config command. Specifically, we need to provide our name and email address because Git embeds this information into each commit we do. We can go ahead and add this information by typing:

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@domain.com"
```
We can display all of the configuration items that have been set by typing:
```bash
git config --list
```
Output
```bash
user.name=Your Name
user.email=youremail@domain.com
```
The information you enter is stored in your Git configuration file, which you can optionally edit by hand with a text editor of your choice like this (we’ll use nano):
```bash
nano ~/.gitconfig
```
~/.gitconfig contents
```bash
[user]
  name = Your Name
  email = youremail@domain.com
```
Press CTRL and X, then Y then ENTER to exit the text editor.

There are many other options that you can set, but these are the two essential ones needed. If you skip this step, you’ll likely see warnings when you commit to Git. This makes more work for you because you will then have to revise the commits you have done with the corrected information.
# Conclusion
You should now have Git installed and ready to use on your system.

To learn more about how to use Git, check out these articles and series:

[How To Use Git Effectively](https://www.digitalocean.com/community/tutorials/how-to-use-git-effectively)
[How To Use Git Branches](https://www.digitalocean.com/community/articles/how-to-use-git-branches)
[An Introduction to Open Source](https://www.digitalocean.com/community/tutorial_series/an-introduction-to-open-source)










