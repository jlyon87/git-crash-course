# Activity 1.2.2 - Merge Conflict

> In this activity

> - Working in pairs.
> - Commit changes to the same file on individual branches.
> - Merge and resolve conflicts of individual branches to `master` branch.

## Instructions

> Using the `merge-activity` repository from the previous activity, we will cause a conflict and resolve it.

## Everyone, Individually

> Apply a change to file-c.txt and push the change to your branch.

1. `git checkout [myBranch]`
2. `git pull`, make sure your local copy is the same as the remote.
3. Add a new line of text to file-c.txt.

  - `Activity-1.2.2 [MyName] made a change to file c on [myBranch]`

4. Add, Commit, and Push your change to your branch.

## Everyone, Together

> There will be a conflict during this merge process. The first person to merge to `master` will have no conflict, anyone merging to `master` after the first will experience the conflict.

1. `git checkout master`
2. `git pull` to make sure your local has the latest from the remote.
3. `git merge [myBranch] --no-ff -m "M - [myBranch] to master"`
4. Open GitKraken to the repository on your machine.

> Use GitKraken to make sure all changes are included in the merge.

1. GitKraken should show a yellow notification for the conflict.
2. Click on the yellow notification.
3. Under the `Conflicted Files` panel in GitKraken, click on the conflicting file.
4. A new panel opens with different versions (`A` and `B`) on left and right, and the final version (`Output`) on the bottom.
5. Use the checkboxes in the `A` and `B` panels to construct the `Output`.
6. When you're done, click `Save`.

> Switch back to your terminal.

1. `git status` to confirm the conflicts are resolved.
2. `git commit -m "M - [mybranch] to master - conflict resolved"`
3. `git push`

> After everyone has merged to master

1. `git checkout [mybranch]`
2. `git merge origin master --no-ff -m "M - master to [myBranch] - downstream"`
3. `git push`

> The `--no-ff` flag is used to maintain a specific branch topology. We want our work to be visually represented on the branches where the work was performed. Without this flag, `git merge` default behavior will attempt simply move the target branch's pointer to the most recent commit. Visually resulting in commits that appear to have occurred on the target branch.

> The `-m` flag on our merge is the same as the flag we use when we commit. It is followed by a message that allows us to name the action we're performing.

> Many commands can be chained in the git CLI. For example to quickly checkout a branch and sync the latest changes from the remote to your local you may enter `git checkout master && git pull`. The double ampersand will chain the commands together sequentially and will stop execution if one of the commands fails.
