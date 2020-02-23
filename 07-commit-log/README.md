# Where are our commits?
For now, they are locally on our machine.

## Inspect commits
```bash
$ git log
commit c6cf8ae52e5cd41fbc808d54b2f26bfb1794ced5 (HEAD -> master)
Author: Victor Velev <victorivelev@gmail.com>
Date:   Wed Feb 5 13:09:06 2020 +0200

    [Fix] 32 x 45 is not 1240, it is 1440

commit 21e6f1168f0a7ef194be8c444f283821d925ecd0
Author: Victor Velev <victorivelev@gmail.com>
Date:   Wed Feb 5 13:02:21 2020 +0200

    [Update] Add mathy_stuff.txt - a multiplication cheat sheet

commit 9451579b4fbe49f6dbcc15b253cd93c45224f70b (origin/master, origin/HEAD)
Author: Victor Velev <victorivelev@gmail.com>
Date:   Wed Feb 5 03:04:19 2020 +0200

    Initial commit
```

We see quite a lot of stuff here.
Lets debunk the log:

## First, we have *commit*
This is essentially a unique commit identifier, you will see later why this is useful.

## Then, *Author* and *Date*
I believe those are pretty self-explanatory.

## And what about the last one? Looks familiar?
Well, this is *our* commit message.

## From there on it repeats.

## We also have ***(HEAD -> master)*** and ***(origin/master, origin/HEAD)***
- **HEAD** is a reference to the last commit made locally.
- **origin**: when you clone a remote repository to your local machine,
git creates an alias for you. In nearly all cases this alias is called "origin."
It's essentially shorthand for the remote repository's URL (in our case "https://github.com/*username*/math-cheat-sheet").
- So **origin/HEAD** is basically the last commit made (*pushed*) in **origin** (this github repo).
- **master** is the main local branch. (We will discuss what a branch is later)
- Analogically, **origin/master** is the master branch of **origin**.

Based on this explanation, we can see that we are (*our local clone of **origin***) is ahead by 2 commits from **origin**.
Git can confirm this:
```bash
$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

## Moving around commits
Use:
```bash
$ git checkout <commit>
```
Where commit is the *unique commit identifier*.

This allows you to move around different versions of your code easily, whithout breaking anything.
Try it out!
