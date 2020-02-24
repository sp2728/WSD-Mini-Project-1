# &#x1F539; Branching in Git &#x1F539;

This section will talk about concept of branching, how to create branches & its uses.

## &#x1F539; Concept of Branching:

In a team working towards same project but on different features, the concept of branching comes in handy. Different branches are created for each feature of the project so that multiple members can work on the project simultaneously, efficiently without dependencies & have a product to deliver early.
By default, a master branch is created in any repository. Then a branch is created for each feature, which can be later deleted once the code is merged with t he master branch.

## &#x1F539; Creating Branches:

Below are the basic steps to create branches using command line:

1. Clone the repsoitory and navigate to the cloned repository using command line.

2. Create a branch using **git branch <branch name>** command.

![](Images/branch_1.png)

3. To view the branch in Github account cloned repository, push the branch to git using **git push origin <branch name>** after performing the edit/add/commit process.

![](Images/branch_2.png)

![](Images/branch_3.png)

## &#x1F539; Resolving the Merge Conflicts:

Merge conflict occurs when people make different changes to the same file on different branches in the repository.

In the pull request list, click the pull request with the merge conflict that you would like to resolve. And click on the resolve conflicts button.

![](Images/mergeConflict1.png)

Decide if you want to keep the incoming changes or the current changes or both the changes. Delete the conflict markers <<<<<<<, =======, >>>>>>> and make the changes you want in the final merge.

![](Images/mergeConflit2.png)

Once all the commits are resolved. Click on the 'commit merge' or 'mark as resolved' button.

![](Images/mergeResolved.png)

And the merge the pull request with master branch

![](Images/mergePullrequest.png)


