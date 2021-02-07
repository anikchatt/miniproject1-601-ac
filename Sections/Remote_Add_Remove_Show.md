[<<< Table of Contents](/README.md)  
[<<< Clone](/Sections/Clone.md)


## Remote Add/Remove/Show


The `git remote` set of commands allow you to manage set of tracked repositories.

* `git remote` alone will show a list of existing remotes.

* `git remote add` adds a new remote to the directory of the repository. 

```
# To set a new remote:

git remote add origin https://github.com/user/repo.git
```
* `git remote rm` this command is known as the remote remove. Git uses *rm* as shorthand for remove. This command will allow one to remove the desired remote. In addition, all the remote-tracking branches and configuration settings for the remote will be removed as well. 

* `git remote show <remote>` will give some information about the remote.

```
$ git remote show origin
* remote origin
  Fetch URL: git@github.com:user/repo.git
  Push URL: git@github.com:user/repo.git
  HEAD branch: main
  Remote branches:
    feature     tracked
    feature1    tracked
    BugFix      tracked
  Local branch cofigured for 'git pull':
    main merges with remote main
  Local ref confugired for 'git push':
    main pushes to main
```
When running `git remote show origin` we get the URL for the remote repository as well as the tracking branch information. It also tells us what branch we are on, and what will happen if we `git pull` or `git push`. 


[>>> Fork](/Sections/Fork.md)
