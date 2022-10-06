# Contributing Guidelines

Hello 👋. We welcome you all to Learn Linux Repository🎊🎊

<br/>

SNo.| Content |
| ---- | ------- |
| 1 | [Contributing guidlines](#contributing-to-this-repository) | 
| 2 | [Basics of git/github](#basics-of-git-and-github) | 


<br/>

## Contributing to this repository
Follow below rules for smooth contribution and create this repo valuable resource <br/>

 **1. See the Issue section** <br/>

Try to make PR to only for open issues. See the issue section for open issues. Get yourself assigned and work on it. Issues that contain "self-assign" tag
are special, anyone can work on them, just follow the rules mentioned in that respective issue.


**NOTE :** If think any area needs modification like content is outdated,typo, improvement you can open that issue by yourself and work on it.

<br/>

**2. Issue Number** <br/>

Mention your issue number on your respective pull request.
You can mention it using a hashtag(#), like for issue 1 : #1

<br/>

### Types of contribution you can make

1. Documentation

- Content Creation in the form of codes or tutorials
- Preferred language should be English
- Markdown Files Accepted
- Clear, Consise and Complete.


<br/>

## Index (readme) files

Inside each directory there is a `README` file. This is the index file of the directory. This `README` file should contain the list of sub-directories 
clicking on which one can navigate to a particular sub-directory. If you are adding a new sub-directory make sure you have added it to the `README` also.
Again, inside subdirectories, there is another `README` file, that will contain all the topics that the subdirectory contains. The point of 
adding `README` inside directories and sub-directories is to help someone know about the content that is residing inside the directory or subdirectory. 

### Not following the contributing guidlines while posting a pull request may lead to an 'invalid' tag in your PR. 

---

<br />

## Basics of Git and GitHub

### Git & GitHub

Before we proceed, it's better to know the difference between Git and Github. Git is a version control system (VCS) that allows us to keep track of the history of our source code , whereas GitHub is a service that hosts Git projects. 

We assume you have created an account on Github and installed Git on your System.

Now enter your name and E-mail (used on Github) address in Git, by using following command.

`$ git config --global user.name "YOUR NAME"`
` $ git config --global user.email "YOUR EMAIL ADDRESS"`
This is an important step to mark your commits to your name and email.

<br />

### Fork a project

You can make a copy of the project to your account. This process is called forking a project to your Github account. On Upper right side of project page on Github, you can see -

<p align="center">  <img  src="https://i.imgur.com/P0n6f97.png">  </p>
Click on fork to create a copy of project to your account. This creates a separate copy for you to work on.

<br />

<br />

### Clone the forked project

You have forked the project you want to contribute to your github account. To get this project on your development machine we use clone command of git.

`$ git clone https://github.com/1Spirit1/Learn-Linux.git` <br/>
Now you have the project on your local machine.

<br />

### Add a remote (upstream) to original project repository

Remote means the remote location of project on Github. By cloning, we have a remote called origin which points to your forked repository. Now we will add a remote to the original repository from where we had forked.

`$ cd <your-forked-project-folder>`
`$ git remote add upstream https://github.com/1Spirit1/Learn-Linux.git` <br/>
You will see the benefits of adding remote later.

<br />

### Synchronizing your fork

Open Source projects have a number of contributors who can push code anytime. So it is necessary to make your forked copy equal with the original repository. The remote added above called Upstream helps in this.

`$ git checkout main`
`$ git fetch upstream`
`$ git merge upstream/main`
`$ git push origin main` <br/>
The last command pushes the latest code to your forked repository on Github. The origin is the remote pointing to your forked repository on github.

<br />

### Create a new branch for a feature or bugfix

Usually, all repositories have a main branch that is regarded to be stable, and any new features should be developed on a separate branch before being 
merged into the main branch. As a result, we should establish a new branch for our feature or bugfix and go to work on the issue. 

`$ git checkout -b <feature-branch>`
This will create a new branch out of master branch. Now start working on the problem and commit your changes.

`$ git add --all`
`$ git commit -m "<commit message>"`
The first command adds all the files or you can add specific files by removing -a and adding the file names. The second command gives a message to your
changes so you can know in future what changes this commit makes. If you are solving an issue on original repository, you should add the issue number
like #35 to your commit message. This will show the reference to commits in the issue.

<br />

### Push code and create a pull request

You now have a new branch containing the modifications you want in the project you forked. Now, push your new branch to your remote github fork. 

`$ git push origin <feature-branch>`
Now you are ready to help the project by opening a pull request means you now tell the project managers to add the feature or bug fix to original repository. You can open a pull request by clicking on green icon -

<p align="center">  <img  src="https://i.imgur.com/aGaqAD5.png">  </p>

Remember your upstream base branch should be main and source should be your feature branch. Click on create pull request and add a name to your pull request. You can also describe your feature.

Awesome! You've already made your first contribution.🥳

#### Happy Contributing 
