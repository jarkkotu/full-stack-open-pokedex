# C# CI setup

## Code formatting and Linting

Code formatting and linting could be done using CSharpier (https://csharpier.com/).
Perhaps the best way would be to configure it in the project to format documents automatically after save, but it could be done automatically in CI as well.
The same tool can be used for linting, i.e. checking if the codes follow the formatting rules

## Unit tests, integration tests, e2e tests

Unit tests and integration tests could be done with .NET built-in library MSTest. Other possibilities are 3rd party testing frameworks NUnit and xUnit.NET.
The syntax is very similar in all of these, so it is really a question of preference.

e2e tests could be run in commercial testing framework Selenium. It supports directly writing tests for web or desktop applications.
But if you would have web application, then I would go with Playwright or Cypress.
It would be also possible to execute javascript written Playwright/Cypress tests from MSTest, if there would be need to set up the environment in C#

## Building

Built using MSBuild

## CI alternatives

Jenkins, GitHub Actions, Azure DevOps

## Self hosted VS cloud environment

If there were no requirement from customer to run the CI/CD pipeline and production enviroment in self hosted servers, then I would use Azure or other cloud environments.
It makes the CI/CD quite simple, and managing the production environment becomes easier.
