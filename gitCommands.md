# Git Commands
## 1. Repository 
A repository is a storage space where your project lives. It can be local to a folder on your computer, or it can be a storage space on GitHub or another online host.

You can create a new repository on your personal account or any organization as shown in the image below:

In the upper-right corner of GitHub page, use the  drop-down menu, and select **New repository**.


![](Images/gitCommands_Repository.png)

In this way, you can create repositories on GitHub. 

You can keep code files, text files, images or any kind of a file in a repository.

## 2. Clone
When you create a repository on GitHub, it exists as a remote repository. You can clone your repository to create a local copy on your computer and synchronize between the two locations.

Basically, Cloning a git repository means that you create a local copy of the code provided by developer. 

You can simply do it with a command line: git clone 

For Example, git clone https://github.com/facebook/facebook-ios-sdk.git.

Following are steps for cloning a repository

(i) On GitHub, navigate to the main page of the repository. Under the repository name, click **Clone or download** as shown in image below.

![](Images/gitCommands_clone1.png)

(ii) To clone the repository using HTTPS, under "Clone with HTTPS", click on that **Clone or download** and copy the link as shown below:

![](Images/gitCommands_Clone2.png)

(iii) Open Git Bash

(iv) Change the current working directory to the location where you want the cloned directory to be made. Type git clone, and then paste the URL you copied in Step 2.

$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY

(v) Press Enter. Your local clone will be created as shown in image screenshot below :

![](Images/gitCommands_Clone3.png)

## 3. Fork
A fork is a copy of a repository that allows you to freely experiment with changes without affecting the original project. 

Forking a project is as easy as clicking the Fork button in the header of a repository. Once the process is complete, you'll be taken right to your the forked copy of the project so you can start collaborating!

If you want to fork someone's repository, then we just have to go to that repository and click on the **Fork** button as shown in image below:

![](Images/gitCommands_Fork.png)

Forking a repository will copy the main data such as files and code. Issues, branches, pull requests and other features, however, will not copy over to your fork.

## 4. Branch

Git Branches plays crucial role in your daily development process. 

In GitHub, they are basically pointers which reflect snapshots of your changes. Whenever you add a new feature, you can just create new branch to enclose your changes. 

This prevents your code to get merged with main code base. 
Master is default branch in github.

The git branch command lets you create, list, rename, and delete branches.

Branches help you organize the workflow of organization more efficiently and rather effortlessly.

You can create new branch in github by using following command : git branch <branch_name>

Below is Image Screenshot which describes the creation of branch workflow :

![](Images/gitCommands_branch1.png)

 






 

