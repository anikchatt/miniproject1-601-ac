[<<< Table of Contents](/README.md)  
[<<< Merge](/Sections/Merge.md)

## Status

`git status` shows the status of changes as untracked, modified or staged.

``` 
$ git status
On branch main
Your branch is up to date with 'origin'

nothing to commit, working tree clean.
```
Git status will tell us what branch we are on, and if our branch is up to date. If any files had been modified, but not staged for a commit, instead of "nothing to commit..." it would read:  
``` 
Changes not staged for commit: 
    modified: File1.md
``` 
If we use `git add` to stage *File1.md* and then use git `git status` the response will tell us that *File1.md* has been staged and is ready to be committed.

[>>> Commit](/Sections/Commit.md)


