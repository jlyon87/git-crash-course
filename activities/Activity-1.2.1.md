# Activity 1.2.1 - Happy Merge

> In this activity

> - Working in pairs.
> - Create multiple branches
> - Commit changes to individual branches
> - Merge individual branches to `master` branch.

## Instructions

> In this activity we'll create a new repository for the group to collaborate on. One person, the group leader, creates the repository on GitHub named `merge-activity`. In the Settings for this new repository, add your group members by their GitHub usernames as Collaborators.

## Group Leader

1. Create a new repository named `merge-activity`.
2. In the new repositories `Settings` Tab, Click `Collaborators`.
3. Add your group members by their GitHub usernames as Collaborators.
4. Clone `merge-activity` to you machine.
5. Again, copy the `/src/` folder from `git-crash-course` repo
6. Add, Commit, and Push this change to `master`.

## Everyone, Individually

> After the group leader has completed their steps, we'll create a scenario where two or more developers are merging their changes to `master`.

1. On GitHub, Accept the invitation to Collaborate from the Group Lead.
2. Create a new Branch under master with your name.
3. Coordinate with your group so each person is modifying a different file within their own branch.

  - `file-a.txt`, `file-b.txt`, or `file-c.txt`

4. Add one new line of text

  - `A-1.2.1 [my name] made a change to [file name].`

5. Add, Commit, and Push the change to your branch.

## Everyone, Together

> After everyone has completed the individual task, merge everyone's branches one at a time to `master`.

1. `git checkout master`
2. `git merge [myBranch] --no-ff -m "M - [myBranch] to master"`
3. `git push`

> After everyone has merged to master

1. `git checkout [mybranch]`
2. `git merge origin master --no-ff -m "M - master to [myBranch] - downstream"`
3. `git push`

> The `--no-ff` flag is used to maintain a specific branch topology. We want our work to be visually represented on the branches where the work was performed. Without this flag, `git merge` default behavior will attempt simply move the target branch's pointer to the most recent commit. Visually resulting in commits that appear to have occurred on the target branch.
