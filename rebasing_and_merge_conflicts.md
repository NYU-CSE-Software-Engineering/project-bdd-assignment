# Local Repo Updating and Merge Conflicts
Do you know how to update your local repo with all the code that will be pushed and merged by your peers?  Find out!
You'll want to update your local repo frequently. One person gathering all changed files from all the team members,
and then submitting one commit/branch/PR is not allowed. You are learning to work collaboratively via git!  Not sure
how to do this? Ask!

Once you update your local repo, you can change to any branch in the repo (for example, `main`, or another branch
authored by your teammates). Consider that you are editing locally from the point when you created your branch locally.
But when you make the PR, obtain a good CR and permission to merge the branch, the branch will likely be behind the most
recent merged code (from your peers). Thus, you will encounter what is known as a _merge conflict_.

You can avoid merge conflicts back when you are editing locally. You might want to look into `rebasing` your branch,
before you push to GitHub. That's likely the easiest way to avoid merge conflicts. However, once you push to GitHub,
merge conflicts might be unavoidable. In that case, when you merge, you will be required to sort through any conflicts
that have arisen. This is code in the repo that is different than what you have and where git is unable to decide which
code to keep. You'll need to research how to specify the correct code to keep in order to resolve the merge conflict so
that the merge can complete.  **THIS IS ALL PART OF LEARNING GIT AND BEING A SERIOUS DEVELOPER WORKING ON A TEAM.**

It is anticipated that you each may have to deal with merge conflicts in this assignment.  They could occur as the
result of your BDD code changes, adding feature files, etc., but also in the design document, and/or in the team-
level index file.  Communications across the team (who is doing what, when they are merging, etc., can _really_ help
here too!)