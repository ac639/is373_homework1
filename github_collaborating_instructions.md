# Collaborating on GitHub

Create a new repository (or go to second line if repo exists) by clicking the + on the right corner of GitHub

Set up the repository and then go to the "Settings" tab.

Click the "Collaborators" button that will appear on the left of the page.

Add a collaborator by adding their GitHub username. The person you are adding will receive
an e-mail to join the repository. When they do they will have full commit  access.

Once all collaborators are added, you can start developing on the repository.

It is recommended for the master branch to kept stable and to make separate branches for developing.

Each collaborator will make his/her own branch on Phpstorm and then commit and push to Github.

You can create a branch in Phpstorm by clcking on the bottom right corner where it says "Git: master" and select "+ New Branch".

![alt text](/img/createbranch.jpg "Phpstorm create branch")

Name your branch and make sure "Checkout" is selected. Your branch will be created and phpstorm will switch you into the new branch

You can start making commits and push to Github. When you push to Github you will notice there will be a new branch.

When you finish with a branch and want switch out and go to another branch, such as master, click the bottom right corner as before and under "Local Branch", select master > Checkout

If you want to merge a branch you worked on into master, switch to master as explained in the previous line.

Click on the menu again and under "Local Branch" select the branch you want to merge into master and then select the option "Merge into Current"

You can then push out master to Github so that your remote master branch is the same as your local.



