[<<< Table of Contents](/README.md)  
[<<< Branch](/Sections/Branch.md)  

## Git-Checkout

`git checkout` allows us to switch branchess. If we are working on the master/main branch, and we create a branch:  

`$ git branch newbranch`  

The HEAD will continue to point to the master/main branch and any edits or changes that we make will be applied to our main branch and not the 'newbranch' that we just created. This is when we use git-checkout to switch to the branch where we would like to make our changes, or edit files.

It is possible to switch to the branch that we just created in one command through the following command:

`$ git checkout -b newbranch`  

This is short for:

`$ git branch newbranch`  
`$ git checkout newbranch`

[>>> Merge](/Sections/Merge.md)



