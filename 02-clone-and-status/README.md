# Now lets get our repo locally (clone it).

### Run the following in your terminal:
```bash
$ git clone https://github.com/<path-to-the-repo>
```

In my case `<path-to-the-repo>` is `VIVelev/math-cheat-sheet`. <br>
In your case it should be `<Your Username>/math-cheat-sheet`.

## Check the `status` of our repo.
```bash
$ cd math-cheat-sheet  # go to our repository
$ git status  # check the status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```

## Several things here:
- First, what does ***On branch master*** mean?
- Second, what does ***Your branch is up to date with 'origin/master'.*** mean?
- And third, what does ***nothing to commit, working tree clean*** mean?

### This word ***branch*** is occuring everywhere... Let's return to it later, and for now look at the third **thing**: ***nothing to commit, working tree clean***

# The staging environment, the commit, and you.

One of the most confusing parts when you're first learning git is the concept of the staging environment and how it relates to a commit.
A commit is a record of what files you have changed since the last time you made a commit. Essentially, you make changes to your repo
(for example, adding a file or modifying one) and then tell git to put those files into a commit. Commits make up the essence of your
project and allow you to go back to the state of a project at any point.

So, how do you tell git which files to put into a commit? This is where the staging environment come in.
Once you've added all the files you want to the staging environment, you can then tell git to package them into a commit. 

### Now that we have the theory behind, lets see how a commit is done.
