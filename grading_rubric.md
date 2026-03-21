# Grading Rubric and Policy

## Grading Rubric

| Criteria                         | Does Not Meet Expectations (0-1)                                                                    | Meets Expectations (2-3)                                                                                       | Exceeds Expectations (4-5)                                                                                    | 
|----------------------------------|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| User Story & Acceptance Criteria | The user story is unclear, incomplete, or does not have testable acceptance criteria.               | A clear user story is provided with at least three testable acceptance criteria.                               | The story and criteria are exceptionally well-defined, clear, and thoughtfully cover the core of the feature. |
| MVC Design Outline               | The MVC outline is missing or does not logically map to the feature described.                      | A reasonable outline of the necessary M, V, and C components is provided.                                      | The MVC outline is detailed and demonstrates a strong understanding of how the feature will be implemented.   |
| Feature File (Gherkin)           | Scenarios are poorly written, do not match the acceptance criteria, or have syntax errors.          | The .feature file is correctly formatted and its scenarios accurately reflect the defined acceptance criteria. | Scenarios are clean, expressive, and cover interesting edge cases beyond the minimum requirements.            |
| Step Definitions (Ruby/Capybara) | The file is missing, contains syntax errors, or does not implement the feature steps with Capybara. | All steps are implemented, and Capybara is used correctly to describe user actions and assertions.             | Step definitions are clean, concise, and demonstrate a strong command of the Capybara API.                    |
| Correctness & Completion         | Deliverables are missing, or the tests do not run correctly.                                        | All required files are submitted. Running Cucumber shows the tests failing for the correct reasons.            | All deliverables are present, and the test output demonstrates a perfect setup for the development phase.     | 

## Grading Policy
While this assignment provides tasks for each team member, it is a "team" assignment.  That is, all the submitted 
files will be reviewed and one overall grade will be assigned (based on the above) rubric for all the work. Members 
of the team will be expected to review each other's work and encourage completeness. Everyone contributes. If someone 
fails to do the work, then there will be a representative deduction for the grade across the board AND the team 
member(s) that do not complete the work will receive no grade.

In support of this policy, we will be looking additionally for the following:
- Each team member should create their own files via their own branch in git.

- Each team member should commit and push their own branch to the repo and create a pull request (PR) for code review. 
When creating the PR, use the "Reviewers" panel to tag one or more team members to request them to review your work.

- Another team member should review your PR for correctness. Are the files complete? Are they in the correct
directories? Are they named correctly? If not, reject the PR and ask the submitter to fix the issues, commit and push
again.  The PR will then require a review again.

When reviewing another member's PR, you should review the files using the "File changed" tab and look at every file. 
See below.

To approve the review, use the "Review Changes" button (the green one shown above) to display the "Finish Your Review" 
window. Leave a comment (required) that acknowledges your review and if you approve the merge, select the correct 
radio button and then click "Submit your review". See image. You can also use this window to request changes to the 
files (in order to reject the PR's merge).

Once approved, the original code submitter can merge the PR to the main/master branch. We will be looking to see 
this process carried out for all team members as they add their files. This is real software development and how 
it works in industry. If you don't understand the process, please ask questions!

Do you know how to update your local repo with all the code that will be pushed by your peers?  Find out! 
You'll want to update your local repo frequently. One person gathering all changed files from all the team members, 
and then submitting one commit/branch/PR is not allowed. You are learning to work collaboratively via git!  Not sure 
how to do this? Ask!