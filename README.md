# cypressiotypescript



Cypress.io for E2E Testing
_______________________________________


Automated testing strategy. As many know manual testing is time-consuming, error prone and can have inconsistent results. An automated testing strategy can set up and test quicker and more reliably than manual testing.  I propose we set up a suite of automated tests that would cover the vast majority of user flows that a typical user would go through.  Once implemented into the continuous integration / continuous development(CI/CD) pipeline this will become a way to test the majority of our app quickly on a per PR basis and will provide quick and effective notifications if something is broken within the pull request.


I would like to suggest the team use Cypress.io framework for our end-to-end(e2e) testing needs. This along with using Github actions to set to run whenever a PR is set to pushed into main will provide a much needed testing boost.  When evaluating a tool or framework I like to think about the following criteria: does it meet our objectives now and will it in the future?  How easy or painless is it to set up and maintain? Does this work well with our current environment or will there need to be a lot of changes to facilitate the change? Is this a new tool? Is there a community and widespread use(aka documentation) which will be valuable when issues arise. Cypress.io works cleanly with our current tech stack, is easy to maintain and has a large user base and community, also their documentation is really good as well.



Other potential automation frameworks
_______________________________________


Playwright


Playwright would also be a solid choice for use for many of the same reasons that cypress.io is. I think the main thing Cypress has over Playwright is that Cypress.io has been around longer, has more of a community around it, has better documentation and is a little easier to set up.  Automatic waiting and Synchronization is much easier to set up on Cypress than Playwright, also cypress.io automatically takes screenshots of defects which can save a lot of time debugging. 


Selenium


Selenium is a much older and much more commonly used automation framework, however it is much more cumbersome to setup, does not have as many nice GUI features and doesn't work as well with modern JavScript frameworks because while Cypress.io can interact with the DOM in real-time, selenium cannot.  Selenium will require multiple WebDrivers to test across multiple browsers, while Cypress.io can test any Chromium browser with the same tests and setup.


Test Cafe


A lightweight framework that works with any browser or mobile and is quick and easy to set up.  It doesn't have all of the features that Cypress has though like the GUI and the automatic debugging and reloading. Also there is less of a community for the framework. 



Getting started with Cypress.io
_______________________________________


Cypress.io is a popular tool for end-to-end testing, making it easy to test web applications. Its ability to simulate real-user interactions make it ideal for verifying an app's behavior.


Open Cypress by running the following command in terminal:


% npx cypress open


Cypress.io is set to automatically run headless however there are GUI options as well for ease of use and debugging. Here are some commonly used Cypress commands for E2E testing:


cy.visit(url): Visit a specific URL.
cy.get(selector): Get an element by CSS selector.
cy.contains(text): Find an element containing specific text.
cy.click(): Simulate a click action.
cy.type('text'): Type into an input field.
cy.should('contain', text): Make an assertion on an element’s content.


Fixtures: Store test data in JSON files under cypress/fixtures and use it in tests by calling cy.fixture('filename').
Screenshots and Videos: Cypress automatically captures screenshots and videos (in headless mode) on test failures.
Environment Variables: Store sensitive data or configuration variables using environment variables in cypress.json or through CYPRESS_* environment variables.




Conclusion
_______________________________________

Cypress will make it easy to write and execute E2E tests for this project. It will ensure that user workflows function as expected. It’s fast and designed for modern applications, making it an excellent choice for our current testing needs.
