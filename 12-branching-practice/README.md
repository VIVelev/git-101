# Working with branches.

Now that we understand what branches are, lets create one and add a new file to it. <br>
After we are done working on this branch, we will merge it with the ***master*** branch.

## Creating a branch.
To create a new branch run the following command:
```bash
$ git branch <new-branch-name>
```

Lets call our new branch - *division-feature*, because we will add a `division-cheat-sheet`.

Run:
```bash
$ git branch division-cheat-sheet
$ git branch  # verify that our branch was created (the asterix prefix - * - denotes the current branch we are in)
  division-cheat-sheet
* master
```

Lets switch to the new branch with `git checkout <branch>`:
```bash
$ git checkout division-cheat-sheet
Switched to branch 'division-cheat-sheet'
```

Git has successfully switched to 'division-cheat-sheet' and now any change we made will be applied only to the branch 'division-cheat-sheet'. <br>
The master branch will be let intact, unless we switch back to it.

## Add the divison cheat sheet:

I will create a new file called `division.txt` with the following content:
```
1 / 2 = 0.5
20 / 5 = 4
```

Now stage and commit, like we already did in master.

## Merge:
To merge `division-cheat-sheet` into master, swithc back to master and run `git merge <branch>`:
```bash
$ git merge division-cheat-sheet
Updating ccfad91..5fa4d46
Fast-forward
 division.txt | 2 ++
 1 file changed, 2 insertions(+)
 create mode 100644 division.txt
```

If you now check the commit log of master, you will see the commit made in `division-cheat-sheet` copied here.
```bash
$ git log
commit 5fa4d46c93ebdc2a1980f57b9b79b570449f5d79 (HEAD -> master, division-cheat-sheet)
Author: Victor Velev <victorivelev@gmail.com>
Date:   Sat Feb 22 15:02:41 2020 +0200

    [Update] add divison cheat sheet

...
```

## Pushing branches.

If you know push your changes from master by `git push`, and go to github.com, you will see only the master branch. <br>
Where is division-cheat-sheet branch we have justed created? Well, it is staying locally on our machine. We have not yet pushed it.

`git push` is an alias for `git push origin <current-branch>` which means:
"Push the commits on branch 'current-branch' to origin (a.k.a. github.com/path-to-repo)."

To push the division-cheat-sheet branch, we need to run:
```bash
$ git push origin division-cheat-sheet
```

Now if you check online, you can see the division-cheat-sheet branch by switching to it from the GitHub UI.
