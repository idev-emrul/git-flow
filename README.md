# git-flow
GitHub workflow by git flow and its steps.

//====================================================================================
GIT FLOW (Github full workflow) 
By: HM Emrul
Developer
Skype: emrul87
//====================================================================================

BRANCHES OF GIT FLOW CONTROL
Master branch 
Develop branch
Feature branch
Release branch
Hotfix branch
Bugfix branch

PRODUCTION RELATIONS BETWEEN DOMAIN AND GITHUB
Master branch will be linked with the public domain for public use. like: www.emptycoder.com
Develop branch will linked with demo domain for testing purpose Like www.demo.emptycoder.com

STEPS TO FOLLOW TO COMPLETE THE FULL GIT LIFECYCLE.
Create a new repository on you github account
Create a new branch develop on current repository
Go to settings options to change the repository name main to master and change default branch master to develop.
Go to your local pc and clone the master branch of the repository where you want to save as local using the following command.
Git clone git-link [Enter]
Initialize git flow to start a git flow chain by using the following commadn.
Git flow init [Enter]
Yes [Enter]
Yes [Enter]
Yes [Enter until finish the input]
Now see you are in develop branch automatically if not in develop use the following command
Git branch checkout develop [Enter]
Push all data to your develop branch for your updated code. Use the following command.
Git push all [Enter]
if this update your code to git develop branch then ok else use following command
Git add .
Git commit  -m ‘First commit to develop branch from local develop branch’
Git push origin develop [Enter]

FEATURE BRANCH
Create new feature branch by following command
Git flow feature start new-feature [Enter]
Now you are in/using feature/new-feature branch automatically if not use following command:
Git branch checkout feature/new-feature
Write your code what you need for your project and push to new-feature branch by following command:
Git add .
Git commit -m ‘Completed or 25% completed of my new feature’
Git push origin feature/new-feature [Enter]
If your assigned feature is completed you think, now you merge your new-feature branch with develop branch by creating a pull request.
Go to your github account and select your current repository.
Click on your pull request. Create a new pull request and follow below steps:
Select develop branch as base and new-feature as compare branch
Marge and squash branch. 
Delete new-feature branch
Go to your local repository
Switch branch feature/new-feature to develop and delete feature branch by following command:
Git branch checkout develop 
Git branch -D feature/new-feature [Enter]
Copy updated data from git repository by pull request by following command:
Git pull origin develop [Enter]
If you need to work on another feature follow the step: [8 to 15]

RELEASE BRANCH
Make a release point or release name by using following command:
Git flow release start 0.0.1 [Enter]
Git push [Enter] (for see the command for set release branch)
Git push - - set-upstream origin release/0.0.1
Go to github repository and click on pull request to merge master with release branch by following steps:
Base as release/0.0.1 branch and  compare with master branch
Only marge [Not marge and squash]
Not delete master branch
Now your repository have three branch as bellow 
 master 
develop 
release/0.0.1

HOTFIX BRANCH
If you think you need an update on the release branch for minor changes you may use hotfix branch to solve this issue.
Select master branch as base branch of hotfix branch by using following command: 
Git branch checkout develop [Enter]
Create a new hotfix branch from master branch by using following command:
Git flow hotfix start new-hotfix [Enter]
Now you are in hotfix/new-hotfix branch if not use the following command:
Git branch checkout hotfix/new-hotfix [Enter] (for use new-hotfix branch)
Write your code as you need. If if you think you need to update your local code to git than make a push using following command:
Git add .
Git commit - m ‘message of your push request on hotfix/new-hotfix branch’ [Enter]
Git push origin hotfix/new-hotfix [Enter]
If you think your hotfix/new-hotfix is completed successfully you may merge and squash the hotfix branch with master branch by following steps:
Goto your github repository and make a pull request and follow following steps:
Master branch as base and hotfix/new-hotfix as compare
Marge only and not delete hotfix/new-hotfix
Complete pull 
Again make a pull request and follow following steps:
Develop as base and hotfix/new-hotfix as compare
Marge and squash then delete the hotfix/new-hotfix branch
Complete pull request
Create a new release branch by following step [ 17 to 19]

BUGFIX BRANCH
If you found any bug on testing time and you need the update of code on the develop branch you may use bugfix branch to solve that issue.
Select develop branch by using following command: 
Git branch checkout develop [Enter]
Create a new hotfix branch by using following command:
Git flow bugfix start new-bugfix [Enter]
Now you are in hotfix/new-hotfix branch if not, use the following command:
Git branch checkout bugfix/new-bugfix [Enter] (for use new-bugfix branch)
Write your code to fix the bug. Then update your local code to github by make a push using following command:
Git add .
Git commit - m ‘message of your push request on bugfix/new-bugfix branch’ [Enter]
Git push origin bugfix/new-bugfix [Enter]
If you think your bugfix/new-bugfix is completed successfully you may merge and squash the bugfix branch with develop branch by following steps:
Goto your github repository and make a pull request and follow following steps:
Develop branch as base and bugfix/new-bugfix as compare
Marge only and not delete bugfix/new-bugfix
Complete pull 
Again make a pull request and follow following steps:
feature/new-feature branch (if have) as base and bugfix/new-bugfix as compare
Marge and squash then delete the bugfix/new-bugfix branch
Complete pull request

===================================================================
END OF GIT FLOW CONTROL INSTARACTION
####################################################################### 
