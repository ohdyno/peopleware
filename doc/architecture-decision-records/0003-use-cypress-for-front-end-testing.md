# 3. Use Cypress for front-end testing

Date: 2023-04-18

## Status

Accepted

## Context

In order to make the software maintainable, we need to be able to test the application and its components.

## Decision

We will use Cypress for component and application testing for the web application.

## Consequences

Cypress supports both component and application testing. Therefore, one likely consequence is that Cypress will
be the only test runner used. This limits unnecessary complexity.

Cypress is a heavier testing application, as it runs the tests within browsers by default. This could introduce
inconsistency in test behavior if the browser versions are different across machines. The inconsistency problem
could be addressed by vendoring browser versions/executables. Another potential challenge with browser-based testing
is running the tests in a headless CI environment. This challenge could be mitigated by using one of the official
CI solutions listed in Cypress's documentation (e.g. CircleCI, Github Actions, etc.).
