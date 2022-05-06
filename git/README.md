

# Git Introduction

## Requirements
For this course an internet access is required and you need to provide an email for the creation of a remote repository. You need a development machine with git installed.

## git basic commands
command | description
------------ | -------------
git clone **url** **[dir]** | copy a Git repository so you can add to it 
git add **file** | adds file contents to the staging area
git commit | records a snapshot of the staging area
git status | view the status of your files in the working directory and staging area 
git diff | shows diff of what is staged and what is modified but unstaged
git help **[command]** | get help info about a particular command
git pull | fetch from a remote repo and try to merge into the current branch
git push | push your new branches and data to a remote repository 
others:    init,    reset,    branch,    checkout,    merge,    log,    tag   | 

## Create the Remote Repositiory on Github
Go to [Github](https://github.com) and create your own github account.

Check the slides for creating your own repo!

## Configure your local git
If you use git the first time you have to configure some things:

```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git config --global user.name "Sebastian Eidner"
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git config --global user.email sebastian.eidner@accenture.com
```

you could choose for example also your default editor:
```
sebastian.eidner@AMAC02DV2DCMD6R firstgitrepo % git config --global core.editor vim
```

If you use ssh you can create a environment file called "ssh_key.env" for example:
```
eval $(ssh-agent)
ssh-add student-1
````

After that you can load this file:
```
. ssh_key.env
```
 or
```
source ssh_key.env
```


## First steps with Git on your machine
In the first exercise, we want create our own local repository and checkin project files.

[Exercise 1](exercise-1/) 

## Get the code to Github
The second exercise shows the steps to push our local repository into our Github account. 

[Exercise 2](exercise-2/) 

## Create a new branch
In the third exercise we will create a branch from our master and push this branch to our Github.

[Exercise 3](exercise-3/) 

## Differences between versions and undo changes
The next exercise will show how you can check changes and undo stuff.

[Exercise 4](exercise-4/) 

## Update the local repo from remote
This exercise will enable you to update your local repo from the remote repository.

[Exercise 5](exercise-5/) 

## Resolve a merge conflict 
The last exercise enables you to resolve merge conflicts, if you are working in teams.

[Exercise 6](exercise-6/) 


## Author(s) and Contacts

- [Sebastian Eidner](http://www.acccenture.com/) | [e-mail](mailto:sebastian.eidner@accenture.com)




