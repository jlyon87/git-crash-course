# git-crash-course

> Most of this course will focus on fundamental usage of git from the command line. You'll need to complete these steps before we can begin our exercises. When you are done, you should have

1. A GitHub Account
2. `git` installed
3. `gitkraken` installed
4. A new empty repository with a `README.md` file.

--------------------------------------------------------------------------------

## Create an Account on GitHub

> GitHub offers free, public repository hosting for everyone. I recommend using a personal email for this account.

1. [Sign Up](https://github.com)
2. Login

--------------------------------------------------------------------------------

## Install

> Follow instructions on these pages to get setup. If you are unsure if you already have `git` installed, open a terminal and type `git --version`.

1. [Install `git`](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
2. [Install `GitKraken`](https://www.gitkraken.com/download)
3. Open a terminal (Mac) or git bash (PC).
4. Type the following commands into the terminal to set your user.

Verify install of git by opening a terminal and typing

```
git --version
```

Enter your User Name and Email for GitHub.

```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

--------------------------------------------------------------------------------

## Create your first Repo

> Create your first repository on GitHub and clone it to your machine.

1. Login to GitHub
2. Click on the `Repositories` tab.
3. Click on the green `New` button.
4. Name your repo, `git-training`.
5. Select `Initialize this repository with a README`.
6. Click the green `Create Repository` button.
7. Click the `Clone or Download` button.
8. Click the Copy to Clipboard icon.

  - Hang onto this for the next step.

--------------------------------------------------------------------------------

## Clone your Repo to your Machine

> After creating your repository on GitHub, you will clone a copy of it to your machine.

> To easily open a terminal on Mac, follow [this guide](https://lifehacker.com/launch-an-os-x-terminal-window-from-a-specific-folder-1466745514)

> To open git bash on PC, open My Documents and right click in the empty space of the folder.

1. Open a terminal on your machine
2. `cd` change directory to My Documents.
3. `mkdir github` to make a new folder for github repositories.
4. `cd github` change directory into the new github folder.
5. `git clone <paste the repository link from github>`

  - `shift + insert` to paste in bash and OSX

6. `cd <repo-name>` After cloning

--------------------------------------------------------------------------------

## Opening a Terminal

### Windows

1. In Explorer, navigate to the folder you want to work in.
2. Right click the folder.
3. Select `Git Bash Here`.

### Mac

> Mac users need to edit their settings to add the terminal to their right click context menu.

1. Follow the guide [here](https://lifehacker.com/launch-an-os-x-terminal-window-from-a-specific-folder-1466745514) to add the Right Click Open Terminal option.
2. In Finder, navigate to the folder you want to work in.
3. Right click the folder.
4. Select `Services` > `New Terminal at Folder`.

--------------------------------------------------------------------------------

## Commands Cheat Sheet

> A quick reference of useful commands.

### Frequently Used

#### `git add .`

After you save a file, add those changes to be tracked.

#### `git commit -m "a message"`

Stage your tracked changes for the next `push`

#### `git push [remote] [branch]`

Push your committed changes to the remote repository branch.

#### `git checkout [branch]`

Switch your local repository to a branch.

#### `git pull [remote] [branch]`

Retrieve the latest from your remote branch into your current branch.

### Infrequently Used

> But VERY handy.

#### `git status`

Check your local repo status compared to the remote.

#### `git remote -v`

Log out the name and url for your repository remote in the cloud.

#### `git checkout -b [newBranch]`

Create a new branch and switch to it on your local repo.

#### `git fetch`

Retrieves latest references from the remote, does not update local repo.
