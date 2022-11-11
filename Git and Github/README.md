# Git Course.

##	Introduction.

Git is a version control system. It’s how as programmers track all the history of their programs. Git is a tool that is used in order to make that kind of track. Github is the website where you can save your project with all the commits that you made.

Each commit has an ID and it shows you the changes made by using color.

##	SSH Keys.

These keys are required in order to authenticate your account and can push code to Github.

1.	ssh-keygen -t rsa -b 4096 -C “email@gmail.com”. Must be the same as your Github account.
2.	It’ll show you where the key will be saved. You can add a different location.
3.	Leave the next commands until you see your key and type ls.

After this, it’ll generate two keys, your public key and your own key. You have to copy all the public key and paste it in your github account. Login in your github account and go to SSH and GPG keys, create a new key, you can write a title for that key and paste it.

##	Branches.

When you are working in a specific project using git, you will be doing your work in the master branch. At the moment you initialize git, it creates by default the master branch and you can create other branches within the project. These branches are called “Feature Branch”.

This is very useful because you can add all the code you need without affecting the original one. Many people can be working in the same project with all the same features. You can test your code to see if it’s working well before to merge it with the main branch.

You can push your changes in a different branch from the master branch to the main project repo (git push -u origin namebranch).

## Pull-request.

The pull request is a request to pull your code into another branch. There are two ways in order to make a pull-request. One is by going to Github repo website or localy.
Probably, you will be editing the same file as other programmer and the conflicts could be appear.

You can solve those conflicts by deleting or changing the files that are in conflict.

## Undo-commits.

You can get back to latest commit in order to undo the changes or the commit made. Once you have add the new changes by typing git add . command, the files change to stage status (green status) and that means that you have already add them to git, but you can unstage that status by typing the git reset command.

## Forking repositories.

You can have a copy from another repository in your github account by forking the project. You will be the admin in the repo copy that you made.

##	Git commands.

* git init. Initialize git within the directory.

* git clone. Make a clone from the project that you want to change or edit (git clone https://url.com.

* git status. It shows all the changes that occurred without adding them to git.

* git add. It adds all the changes that you did in your files (git add . || git add name.txt).

* git commit. Save your files in Git. Command -m means message (git commit -m “New commit”). You can add a title and a message on each commit by adding an extra -m “” at the end of the command line.

* git commit -am. It's a shortcut for git add and git commit. YOu can use this command once the file was added to git.

* git log. Once you use this command, you will see all the commits that you made.

* git remote. You can set the repo’s link in order to upload your project to github (git remote add origin https://url.com

* git remote -v. It displays all the repo that are connected to this project.

* git push. Upload all the git commits made to a remote repo. You can define a default origin by adding -u when you declare your first commit (git push -u origin master).

* git branch. It creates a branch (git branch Jorge).

* git branch -d namebranch. It deletes the branch created,

* git branch -D namebranch. It forces to delete the featured branch.

* git merge. Merge all the commits made in a feature branch with the master branch.

* git checkout. You can jump between branches using this command (git checkout Jorge).

* git checkout -b namebranch. It creates a feature branch and it takes you to this new branch created.

* git diff. It shows you the changes that your have made (git diff namebranch).

* git pull. It downloads the changes from a remote repo to your local machine. This is helpul if you make changes online and have them in your local enviroment.

* git reset. It resets the commit where you were working on.

* git reset HEAD~1. It takes you to the latest commit further.

* git reset XX53X. This command take you back to an specific commit. You have to type the hash value.

* git reset --hard ZXXFW. If you want to delete all the changes and lines that you wrote in your code before making the commit action, use this command in order to restore each file.

## Author.

* Jorge Ortiz.
* Software engineer at Icalia Labs.
* San Luis Potosí S.L.P. México.
* +52 (444) 576 3034.

Have a Wonderul Day!.
