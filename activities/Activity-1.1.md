# Activity 1.1 - Branch & Commit

> In this activity

> - Copy Files from another repo.
> - Practice `add`, `commit`, & `push` changes to branches in your repo.
> - Create a branch

## Instructions

> On your machine follow these steps.

1. Goto [our training repo](https://github.com/jlyon87/git-crash-course) and retrieve the Clone Url
2. Open a terminal to `../My Documents/github`
3. Enter the command `git clone <git-crash-course clone url>`
4. Copy the `/src/` folder from this repo into your `git-training` repo from the previous activity.
5. Open a terminal to `git-training`.
6. Enter `git status`. You should see the added `/src/` folder.
7. Enter `git add .` to add this change to git's tracked changes.
8. Enter `git commit -m "adding activity 1.1 source"` to stage these tracked changes.
9. Enter `git push origin master` to push the staged changes to the remote `git-training` repo.

## Create a Branch

> Create a branch locally and push it to the remote.

1. Enter `git checkout -b dev`

  - This has created a new branch on your local repo named `dev`.

2. Enter `git push -u origin dev`

  - This pushes the new branch to the remote, creating it on github.

## Commit a change to `dev`

> Apply a change to a file and push it to a branch.

1. Open file-a.txt and add a new line:

  - `I'm making a change to file-a.`.

2. Save file-a.txt.
3. In your terminal, Enter `git status`.

  - Confirm the saved file is there.

4. Add the file to git's tracked changes.
5. Enter `git status` again to see it's being tracked.
6. Commit the tracked changes with the commit message "A-1.1 update file-a"
7. Push the staged changes to dev.
