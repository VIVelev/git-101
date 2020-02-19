# Creating a commit.

Lets check our repo again.

```bash
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   mathy_stuff.txt

```

Greate news, git realised that we would like to have `mathy_stuff.txt` in our next commit
and has told us that it is in `Changes to be committed`.

## So how do we make a **commit**?
Well, simple:
```bash
$ git commit -m "<commit-message>"
```

Lets make one:
```
$ git commit -m "[Update] Add mathy_stuff.txt - a multiplication cheat sheet"
```

## Quick Tips
- Your commit messages should be descriptive, please don't make commit messages such as:
  - "some stuff"
  - "i am hungry"
  - "."

- Follow a simple patter to distinguish between types of commits:
  - Addition / Modification (I suggest "[Update] ...")
  - Removal (I suggest "[Remove] ...")
  - Fixes (I suggest "[Fix] ...")
