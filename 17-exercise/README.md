# git & GitHub Exercise

The following practical exercise should give you some familiarity with using 
git. 

Note: The provided command line examples are to remind you of the correct syntax 
and keywords, and won't necessarily work if you type them in blindly

Other Note: to get help on a particular git command, use `git <command> --help`

## Setup
1. Install and setup git on your computer (remember to set your name/email)

    ```bash
    $ git config --global user.name "Firstname Lastname"
    $ git config --global user.email "example@maths.ox.ac.uk"
    ```

2. Create an account (or login) to GitHub at <https://github.com> 

3. Create a new repository

## Exercise 1: Making Commits

1. Clone the repository you have just made to your computer

    ```bash
    $ git clone <url>
    ```

2. Create and add a new file to the staging environment

    ```bash
    $ git add <file>
    ```

3. Commit the new file

    ```bash
    $ git commit -m "message"
    ```

4. Examine the state of your repo with `git status`. 

    ```bash
    $ git status
    ```

5. Edit and save your new file, then add it to the staging area. Finally make a 
   new commit with the edited file. At all stages use `git status` to see how 
   your repository changes

    ```bash
    $ git add <file>
    $ git commit -m "message"
    ```

6. Make some more commits and view the log

    ```bash
    $ git log 
    ```

7. Push the commits to the server

    ```bash
    $ git push
    ```

## Exercise 2: Branching and Merging

1. Create a new branch 

    ```bash
    $ git branch new_branch
    ```

2. Edit your file and commit the changes in the new branch

3. Swap back to the master branch

    ```bash
    $ git checkout master
    ```

4. Merge `new_branch` to `master`

    ```bash
    $ git merge new_branch
    ```

5. Now create conflicting commits in `new_branch` and `master` and try to merge 
   them. Note the conflict-resolution markers will look something like this.

    ~~~~~~bash
    <<<<<<< HEAD
    This is the new line in master
    =======
    This is the new line in branch
    >>>>>>> branch
    ~~~~~~

6. Resolve the conflict (i.e. edit the conflict markers to match how you want 
   the file to look like) and commit the result. Use `git log` to see the 
   resulting commits on the master branch.

## Exercise 3: Collaboration

1. Push the new branch that you created in the previous exercise to your remote 
   repository

    ```bash
    $ git push origin new_branch
    ```

2. Get a friend/teammate to clone your repository and checkout your 
   new branch. 

    ```bash
    $ git checkout new_branch
    ```

3. Both of you make commits to the new branch. Have one person push their 
   commits and the other merge these with their own commits. Swap 
   roles and repeat the process. 

4. Once you are happy with the state of your new branch, merge it onto your 
   `master` branch and bask in the glow of your new git skills. :)
