# How to get the latest changes locally?

Now we know that we are not up-to-date. But, how do we get the latest changes locally?
Lets *pull* the latest changes.
```bash
$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 687 bytes | 343.00 KiB/s, done.
From https://github.com/VIVelev/math-cheat-sheet
   a764533..359ca1e  master     -> origin/master
Updating a764533..359ca1e
Fast-forward
 mathy_stuff.txt | 4 ++--
 1 file changed, 2 insertions(+), 2 deletions(-)
```

Cool, just as we expected:
```bash
1 file changed, 2 insertions(+), 2 deletions(-)
```

Here by `2 insertions` is ment `2 new lines were added`.
And by `2 deletions` - `2 lines were deleted`.


Lets check the content of `mathy_stuff.txt`:
```bash
$ cat mathy_stuff.txt
1 x 2 = 2
blablabla
tralalal tralala
```

Great! Well, actually, not so great... <br>
Our math-cheat-sheet is now garbage, because of some idiot who changed it online...

Lets fix that in the next chapter.
