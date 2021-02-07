[<<< Table of Contents](/README.md)  
[<<< Push](/Sections/Push.md)


## Git-Pull

`git pull` updates the local branch that you are currently checked out to with any new commits that have been on the remote [branch](/Sections/Branch.md) of the same repository. **git pull** is shorthand for **git fetch** followed by **git merge** to merge the retrieved branch heads into the current branch.

For example, when contributing to an existing branch on Github, on a project called 'miniproject' and after having cloned it:

```
# change into the desired directory
cd miniproject

# use git-pull to update all remote branches, and the currently checkout out branch
git pull

# make the changes and edits that you desire to the file 'File1.md'

# stage the file
git add File1.md

# commit the changes
git commit -m 'Feature: edited File1'

# push the changes to gitHub
git push
```

In the above example, the changes that were made locally were pushed to the remote repository on Github. Assuming you were working on a different branch and not the main/master branch, the changes that were made locally will only be reflected on that same branch remotely. Towards the end of your project, when it is time to merge your contributions with everyone, you can initiate a ***Pull Request***. 

A *pull request* allows you to share and discuss the changes that you made with your teammates, it is also a request to update the main branch with the changes that were made on the feature branch that you were working on. When a *pull request* is approved, the next step would be to merge the pull request to the master branch. 


 

### Read more:
* [git-fetch](https://git-scm.com/docs/git-fetch)


##### To view all the sources used in this project, [click here!](/Sources.md)

[>>> Table of Contents](/README.md)





           