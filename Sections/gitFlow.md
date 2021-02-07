[<<< Table of Contents](/README.md)
## GitFlow 

# What is GitFlow? 

GitFlow is the branching development model for Git designed by Vincent Driessen. Using GitFlow helps developers throughout the software development process. The key benefits of leveraging the Git Workflow include parallel development, collaboration, release staging area, and support for emergency fixes. The idea behind this workflow is to identify what branches are needed and how they should interact with each other. 

# Main Branches

After creating a [repository](/Sections/Repository.md) that includes a [Main Branch](/Sections/Master.md) that will be deployed to Production, the developer should create another [branch](/Sections/Branch.md) that is parallel to the main branch, development. The development branch will act as an integration branch for features that are included throughout the development process. To create a new branch named development and push it to the existing repository the developer can do: 
```
$ git branch development 
$ git push -u origin development
```
When working with other developers, they should clone the repository and begin tracking the development branch. Once all the developers have completed their work out of their feature branches (will be discussed below) they should merge them into the development branch. 

# Supporting Branches 

The types of the supporting branches are feature, release, and hotfix. The benefits of using these supporting branches are that they provide opportunities for developers to easily track features and assist to debug problems that may arise from production. 

* Feature Branch: Feature branches typically branch off the development branch and  [merge](/Sections/Merge.md) back into the development branch. The purpose of a feature branch is to allow multiple developers to work on a specific task without interacting with the main branch. To create a new feature branch from development and merge the feature branch back into the development branch the developer can do: 
```
 $ git checkout -b feature_branch1
 $ git checkout development
 $ git merge feature_branch1 
```

* Release Branch: Release branches are meant to be created once the development branch has reached a stage that it is ready for merging with the master branch. The release branch can be used to make small bug fixes before deployment, but should not be used to add in new features. To create a new release branch from development and merge the release branch back into the main and development branch the developer can do: 
```
 $ git checkout -b release/0.0.1
 $ git checkout development
 $ git merge release/0.0.1 
 $ git checkout main
 $ git checkout release/0.0.1
```

* Hotfix Branch: Hotfix branches are meant to fix any bugs that may have risen within the code once it is released into production. This type of branch is similar to a release branch as it is not meant to contain too many changes, and only necessary to fix the issues that arise. Hotfix branches are meant to be branched off from the main branch and be merged back into the development/main branch so the changes that were made can be tracked. 
```
 $ git checkout -b hotfix_b1
 $ git checkout development
 $ git merge hotfix_b1
 $ git checkout main
 $ git checkout hotfix_b1
```

# Summary 

Using GitFlow is very helpful and easy to implement within a software development team. The overall flow for the GitFlow methodology is a development branch is created from the main branch. Then a feature branch is are created from the development branch and merged back into the development branch. A release branch is created from the development branch and is merged into the main and development branch. Finally, if an issue in production is noticed, a hotfix branch is created from the main branch, once the hotfix branch is completed it is merged back into the main and development branches. A diagram of the GitFlow Process can be seen below:

 
![GitFlow Diagram](/images/gitFlow.PNG)  
   
  
[Repository >>>](/Sections/Repository.md)