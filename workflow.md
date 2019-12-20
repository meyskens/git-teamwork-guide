# GitHub teamwork workflow

In the past you already learned how to use GitHub and Git to do versioncontrol on your projects.  
In this tutorial we're going one step further and use Git to allow working in team on the same codebase.

## Setting up your repository
// TODO: add base repo
// TODO: add contributors


## Working with branches
After you cloned the project on your computer we can start working on code changes. We do this in branches.
Branches, also called feature branches, make a copy of the main code which resides on the "master" branch.
It is a bad practice to push directly to the "master" branch when working in teams. An exception for this rule us the first commit.
In a branch you can make one or more commits as usual, these reflect the changes to add a certain part of the code. 
To make a new branch you can do the following using Git
```sh
$ git branch [branch name]
```
The branch name should contain the part you plan to add, as well as your name so you have no conflicts with your teammates.
A name for example could be `maartje-add-contact-page`, note that branch names cannot contain spaces!

Creating branches is done using `git branch`. After creating the branch you have to switch to using that branch.
This can be done using `git checkout`.
```sh
$ git checkout [branch name]
```
This command will change your files on your hard disk to reflect those in the branch.

You can now work as usual and use `git add` and `git commit` to commit your changes.
You can use `git push` when on a branch to push the branch to GitHub
// TODO: confirm you need --set-upstream

A full workflow for example would be
```
$ git branch maartje-add-contact-page
$ git checkout maartje-add-contact-page
$ touch contact.html # Example change!!! not part of the workflow
$ git add .
$ git commit -m "Created a contact page"
$ git push
```

## Pull Requests

