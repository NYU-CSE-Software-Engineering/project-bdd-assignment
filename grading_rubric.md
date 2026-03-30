# Grading Policy, Team and Individual Grading Rubrics, and Rebasing/Merge Conflicts

## Grading Policy

While this assignment provides tasks for each team member, it is graded both as a "team" assignment and with some
validation of individual responsibilities. That is, the submitted files will be reviewed and team-level rubrics will be
checked, but an individual set of rubrics exist for individual expectations.

Members of the team will be expected to review each other's work and encourage completeness. Everyone contributes. If
someone fails to do their portion of the work, then there will be a representative deduction for the grade for all
team members, since it is the team's responsibility to complete the assignment. Of course, if a team member does not
contribute to the BDD work, then it is also likely their individual rubric items would be negatively impacted
the board AND the team member(s) that do not complete the work will receive no grade.

In support of this policy, we will be looking at the following:

- Each team member will author at least 1 branch for each BDD feature implemented (see "Your Tasks" in the
  [README file](README.md)). Thus, we should see not less than 3 branches for your work (more is fine, if necessary).
- Each created branch will be committed locally, pushed to the team's repo on GitHub. And a corresponding pull request
  (PR) will be created.
- When a PR is created, the author must put in a 2-3 sentences of a description of the purpose of the PR.
- The PR author will both:
    - use the "Reviewers" panel to tag one or more team members to request them to review your work, and
    - use the "@username" to ask a team member/s for a code review
- Each team member should code review at least 4 pull requests for other members of their team. Team members CAN NOT
  code review their own PRs. Code reviews can have more than one reviewer. All pull requests must include non-trivial
  code review comments by the review and gain the approval to merge the PR, if appropriate (see next item).
- Team members doing code reviews should review the PR for functional correctness. Are the files complete? Are they in
  the correct directories? Are they named correctly? If not, reject the PR and ask the author to fix the issues, then to
  commit those files again locally to the branch, and to push the branch again to GitHub. This will add the new commit
  files to the PR and the PR needs to be code reviewed again.

- ## Team Grading Rubric (Max. 29 points)

| Criteria                         | Does Not Meet Expectations (0-1 pts.)                                                               | Meets Expectations (2-3 pts.)                                                                                  | Exceeds Expectations (4-5 pts.)                                                                                                                                | 
|----------------------------------|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| User Story & Acceptance Criteria | The user story is unclear, incomplete, or does not have testable acceptance criteria.               | A clear user story is provided with at least three testable acceptance criteria.                               | The story and criteria are exceptionally well-defined, clear, and thoughtfully cover the core of the feature.                                                  |
| MVC Design Outline               | The MVC outline is missing or does not logically map to the feature described.                      | A reasonable outline of the necessary M, V, and C components is provided.                                      | The MVC outline is detailed and demonstrates a strong understanding of how the feature will be implemented.                                                    |
| Feature File (Gherkin)           | Scenarios are poorly written, do not match the acceptance criteria, or have syntax errors.          | The .feature file is correctly formatted and its scenarios accurately reflect the defined acceptance criteria. | Scenarios are clean, expressive, and cover interesting edge cases beyond the minimum requirements.                                                             |
| Step Definitions (Ruby/Capybara) | The file is missing, contains syntax errors, or does not implement the feature steps with Capybara. | All steps are implemented, and Capybara is used correctly to describe user actions and assertions.             | Step definitions are clean, concise, and demonstrate a strong command of the Capybara API.                                                                     |
| Correctness & Completion         | Deliverables are missing, or the tests do not run correctly.                                        | All required files are submitted. Running Cucumber shows the tests failing for the correct reasons.            | All deliverables are present, all tests pass when `bundle exec cucumber` when run, and the test output demonstrates a perfect setup for the development phase. | 

| Criteria / Deliverables Location	                  | Met Requirement (1 pts.) | Failed to Meet Requirement (0 pts.) |
|----------------------------------------------------|--------------------------|-------------------------------------|
| BDD Feature Files: `features/*.feature`            |                          |                                     |		
| Step Definitions: `features/step_definitions/*.rb` |                          |                                     |
| Cucumber Support Files: `features/support/`        |                          |                                     |

## Individual Grading Rubric (Max. 18 points)

| Criteria                                                                                                                                           | Meets Criteria (3 pts.) | Fails To Meet Criteria (0 pts.) |
|----------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|---------------------------------|
| Member created at least 3 branches / pull requests for BDD work. Pull request contains intelligent non-trivial comment                             |                         |                                 |
| Member's pull request correctly tags code request of teammate's userid in both the Reviews panel and in the comment field.                         |                         |                                 |
| Member performed code reviews for 4 or more pull requests of other teammate's pull request. Code review includes non-trivial comments by reviewer. |                         |                                 |
| Member's pull request obtained approval for merger through the code review process of at least 1 teammate.                                         |                         |                                 |
| Member performs merge to `main` branch of the branch/pull request they opened/created.                                                             |                         |                                 |
| Member did not merge another member's branch/pull request.                                                                                         |                         |                                 |

