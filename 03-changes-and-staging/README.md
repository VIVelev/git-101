# Let's create a simple multiplication cheat sheet.

## Open your favorite text editor and write some mathy stuff like:
```
1 x 2 = 2
2 x 2 = 4
32 x 45 = 1240
```

## Check the status now:
```bash
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	mathy_stuff.txt

nothing added to commit but untracked files present (use "git add" to track)
```

It looks like we have a new field - ***Untracked files***

This pretty much tells us that git hase *seen* that we have made changes in our repository.
More specifically it tells us "Hey, it seems like you have add a new file called 'mathy_stuff.txt', but I am not gonna do
anything about it unless you add it to the staging environment."

## How to add a file to the staging environment?
Simple:
```bash
$ git add <file>
```
Just as `git status` told us.

So lets add `mathy_stuff.txt` to the staging environment. In that way we let git know that we would like
to include `mathy_stuff.txt` in out next commit.

```bash
git add mathy_stuff.txt
```

Next, we will make a commit, excited? :)

## Quick Tip
Most of the time you will find yourself using this command:
```bash
$ git add .
```

This essentially adds all changed/added files to the staging environment.
