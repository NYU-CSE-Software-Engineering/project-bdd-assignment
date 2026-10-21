# Grading Policy, Team and Individual Grading Rubrics, and Rebasing/Merge Conflicts

## Grading Policy

While this assignment provides tasks for each team member, it is graded both as a "team" assignment and with some
validation of individual responsibilities. That is, the submitted files will be reviewed and team-level rubrics will be
checked, but an individual set of rubrics exist for individual expectations.

Members of the team will be expected to review each other's work and encourage completeness. Everyone contributes. If 
a team member does not contribute to the BDD work, then their individual rubric items would be negatively impacted across
the board AND the team member(s) that do not complete the work will receive no credit for the team's work.

In support of this policy, we will be looking at the following:

- Each team member will author **at least 1 branch for each BDD feature implemented** (see "Your Tasks" in the
  [README file](README.md)). Thus, we should see not less than 3 branches for your work (more is fine, if necessary).
- Each created branch will be committed locally, pushed to the team's repo on GitHub, and a corresponding pull request
  (PR) will be created.
- When a PR is created, the author **must put in a 2-3 sentence description** of the purpose of the PR.
- The PR author will both:
    - use the "Reviewers" panel to tag one or more team members to request them to review your work, **and**
    - use the "@username" to ask a team member/s for a code review
- Each team member will provide a code review of not less than 3 pull requests for other members of their team. Team
  members CAN NOT code review their own PRs. Code reviews can have more than one reviewer, but must have at least one.
  All pull requests must include **non-trivial code review comments** by the review and gain the approval to merge the PR,
  if appropriate (see next item).
- Team members doing code reviews should review the PR for functional correctness. Are the files complete? Are they in
  the correct directories? Are they named correctly? If not, reject the PR and ask the author to fix the issues, then to
  commit those files again locally to the branch, and to push the branch again to GitHub. This will add the new commit
  files to the PR and the PR needs to be code reviewed again.
- Once approved, **the author of the branch/PR must merge their code**. Do not merge someone else's branch. 

## Team Grading Rubric (Max. 30 points)

| Criteria                         | Exceeds Expectations (4-5 pts.)                                                                                                                                      | Meets Expectations (2-3 pts.)                                                                                  | Does Not Meet Expectations (0-1 pts.)                                                               | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| User Story & Acceptance Criteria | Each user story and its criteria are exceptionally well-defined, clear, and thoughtfully cover the core of the feature.                                                        | Each user story is provided with at least three testable acceptance criteria.                               | Any user story is unclear, incomplete, or does not have testable acceptance criteria.               |
| MVC Design Outline               | The MVC outline is detailed and demonstrates a strong understanding of how the feature will be implemented.                                                          | A reasonable outline of the necessary M, V, and C components is provided.                                      | The MVC outline is missing or does not logically map to the feature described.                      |
| Feature File (Gherkin)           | Scenarios are clean, expressive, and cover interesting edge cases beyond the minimum requirements.                                                                   | The .feature file is correctly formatted, and its scenarios accurately reflect the defined acceptance criteria. | Scenarios are poorly written, do not match the acceptance criteria, or have syntax errors.          |
| Step Definitions (Ruby/Capybara) | Step definitions are clean, concise, and demonstrate a strong command of the Capybara API.                                                                           | All steps are implemented, and Capybara is used correctly to describe user actions and assertions.             | The file is missing, contains syntax errors, or does not implement the feature steps with Capybara. |
| Correctness & Completion         | All deliverables are present, all tests fail (for the correct reasons) when `bundle exec cucumber` is run, and screenshots of failing tests are delivered as required. | Most required files are submitted. Some files are incomplete or lacking depth.                                 | Deliverables are missing or are grossly incomplete.                                                 | 

| Criteria / Deliverables Location	                   | Met Requirement (1 pts.) | Failed to Meet Requirement (0 pts.) |
|-----------------------------------------------------|--------------------------|-------------------------------------|
| Team-level index File: `docs/team_feature_index.md` |                          |                                     |
| BDD Feature Files: `features/*.feature`             |                          |                                     |		
| Step Definitions: `features/step_definitions/*.rb`  |                          |                                     |
| Cucumber Support Files: `features/support/`         |                          |                                     |
| Screenshot Files: `features/screenshots/`           |                          |                                     |

## Individual Grading Rubric (Max. 21 points)

| Criteria                                                                                                                                            | Meets Criteria (3 pts.) | Fails To Meet Criteria (0 pts.) |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|---------------------------------|
| Member created at least 3 branches / pull requests for BDD work. Each pull request contains an intelligent, non-trivial 2-3 sentence description.   |                         |                                 |
| Member's pull request correctly tags code review request of teammate's userid in both the Reviews panel and in the comment field using @ notation.  |                         |                                 |
| Member performed code reviews for 3 or more pull requests of other teammates' pull requests. Code review includes non-trivial comments by the reviewer. |                         |                                 |
| Member's pull request obtained approval for merge through the code review process of at least 1 teammate.                                          |                         |                                 |
| Member performs a merge to the `main` branch of the branch/pull request they opened/created.                                                              |                         |                                 |
| Member did not merge another member's branch/pull request.                                                                                          |                         |                                 |
| Member did not code review their own branch/pull request.                                                                                           |                         |
