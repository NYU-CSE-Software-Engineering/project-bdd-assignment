# Project Design: Behavior-Driven Development

## Objective
The goal of this assignment is to refine the design of your proposed team project by applying Behavior-Driven Development (BDD) principles. Each member of the team will select a feature of your application, translate its requirements into multiple detailed user stories, and create a full set of acceptance tests that specify its behavior. In support of this, some of the project software may need to be implemented.

You will use Cucumber and Capybara to create these specifications. This exercise will force you to think through user interaction and application logic before writing any significant implementation code for your own project.

## Background
Behavior-Driven Development is a software development process that bridges the gap between technical implementation and business requirements. By writing specifications in a natural, human-readable language, you ensure that your project's features are well-defined and meet user expectations from the start.

[Cucumber](https://cucumber.io/) is a tool that reads plain-text specifications (written in Gherkin) and executes them as automated tests. See [this link](https://cucumber.io/docs/gherkin/reference) for the syntax reference. And [here's a link](https://cucumber.io/docs/guides/10-minute-tutorial/?lang=ruby) to a 10-minute tutorial.

[Capybara](https://teamcapybara.github.io/capybara/) is a library that simulates how a user interacts with your web application, allowing you to test the application from an external, user-centric perspective.

For this assignment, you will use these tools to create a detailed, testable design for a key part of your application.

## Your Tasks
Each member of the team is required to select **three core features** from your proposed project, develop the user stories associated with those features, and create the necessary files to specify and test their behavior. Each feature selected by each team member should be distinct from those features that the other team members are completing.

### Task 1: Define Your Features with User Stories

Before writing any tests, you must clearly define each feature.

* **Create a Design Document**: In the `docs/` directory of your project, each team member should create a new file named `docs/<your_feature_name>.md`. One team member should create a single `docs/<team_feature_index>.md` file that links to all of the feature story files from the team. (See the slides from Chapter 7 for a reminder about user stories.)

* **Write the User Story**: Inside this file, write a single user story for your feature. Thus, each team member will create two unique files that detail the user story for their selected features. The story should follow the standard format: _"As a [type of user], I want to [perform some task] so that I can [achieve some goal]."_

* **Define Acceptance Criteria**: Below the user story, list three to five specific, testable acceptance criteria. These will define what it means for the feature to be "complete" and will form the basis of your test scenarios. Consider your "happy" and "sad" paths as candidates to include.

### Task 2: Outline the MVC Components

In the same `.md` file, briefly describe the Models, Views, and Controllers you anticipate needing to build this feature. This helps connect your BDD specification to the underlying MVC architecture. The MVC bullets below provide brief examples related to a hypothetical blog posting application.

* Model(s): What data is involved? What new models or model attributes will you need? (e.g., _"A Post model with title:string and content:text attributes."_)

* View(s): What new pages or page components will the user see? (e.g., _"A posts/new.html.erb view with a form."_)

* Controller(s): What new controller actions will be required to handle user requests? (e.g., _"A PostsController with new and create actions."_)

### Task 3: Create the Feature File

Translate your user story and acceptance criteria into a [Gherkin](https://cucumber.io/docs/gherkin/reference/) feature file.

1. **Create the file**: In your Rails project, create a new file under the `features/` directory (e.g., `features/creating_a_post.feature`).

2. **Write the specification**: Write scenarios that test your acceptance criteria. You should have at least one "happy path" (success) scenario and at least one failure or edge-case scenario.

#### Example Gherkin Structure (for a blog post feature):
```
Feature: Create a new blog post
  As a signed-in user
  I want to publish a new post
  So that I can share my thoughts with others

Scenario: User creates a post with valid information
  Given I am a signed-in user
  And I am on the new post page
  When I fill in "Title" with "My First Post"
  And I fill in "Content" with "This is the content of my post."
  And I press "Create Post"
  Then I should be on the post's show page
  And I should see the message "Post was successfully created."
  And I should see the title "My First Post"

Scenario: User fails to create a post without a title
  Given I am a signed-in user
  And I am on the new post page
  When I fill in "Content" with "This post has no title."
  And I press "Create Post"
  Then I should see an error message indicating the title is missing
```

### Task 4: Generate and Implement Step Definitions

Translate the Gherkin steps into executable Ruby code using Capybara.
1. **Run Cucumber**: From your Docker shell, run `cucumber` to get the pending step definition snippets.

2. **Create the Step Definition File**: Create a new file for your steps (e.g., `features/step_definitions/post_steps.rb`).

3. **Implement the Steps**: Copy the snippets into your new file and replace the pending comments with Capybara actions.

#### Example Implementation Snippet (`post_steps.rb`):
```
Given("I am a signed-in user") do
  # This step requires you to create a user and simulate a login.
  # For now, you can model this with a user created in the test database.
  @user = User.create!(email: 'test@example.com', password: 'password')
  visit new_user_session_path
  fill_in 'Email', with: @user.email
  fill_in 'Password', with: @user.password
  click_button 'Log in'
end

Given("I am on the new post page") do
  visit new_post_path
end

Then("I should be on the post's show page") do
  # This is tricky before the model exists!
  # A good "Red" step might just check for the content.
  expect(page).to have_content("My First Post")
end

Then("I should see an error message indicating the title is missing") do
  expect(page).to have_content("Title can't be blank")
end
```

## Deliverables

Commit and push the following files to your project repository:
1. For each of your two features, a design document `docs/<your_feature_name>.md` containing your user story, acceptance criteria, and MVC component outline (you will therefore have two such files).
2. For each of your two features, a Gherkin feature file `features/<your_feature_name>.feature` describing the scenarios for that feature.
3. For each of your two features, corresponding Ruby step definitions in `features/step_definitions/<your_steps>.rb` that implement all of the steps used in your feature files (you may organize these in one or more files, but they must cover both of your features).
4. For each of your two features, at least one screenshot `features/screenshots/<your_feature_name_N>.jpg` (where N is a number) of your shell/terminal after running Cucumber, showing the failing test output for your scenarios.
5. A single team-level index file (created by one team member) in `docs/<team_feature_index>.md` that links to all of the feature-story design documents (`docs/<your_feature_name>.md`) for every team member.

## Addendum

- [Addendum](addendum.md)

## Grading Rubric

- [Grading Rubric](grading_rubric.md)