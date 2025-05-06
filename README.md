# Syntestio Starter Template

This repository serves as a starter template for creating automated tests using Syntestio - an AI-powered test automation tool. It provides the basic structure and configuration files to help you quickly get started with Syntestio testing.

## Repository Structure

- **tests/**: Contains test files with scenarios written in Gherkin syntax

  - **features/**: Holds feature files that define test scenarios
    - **sample.feature**: Example feature file showing the structure of Gherkin test scenarios

- **config.json**: Configuration file for local test execution
- **config.ci.json**: Configuration file optimized for CI pipeline execution

## Getting Started

### 1. Configure your environment

Update both configuration files with your Syntestio API key and application URL:

```json
// In config.json and config.ci.json
{
  "apiKey": "YOUR_API_KEY_HERE",
  "appUrl": "YOUR_APP_URL_HERE",
  ...
}
```

### 2. Create your test scenarios

Rename and modify the sample feature file `tests/features/sample.feature` to contain your actual test scenarios. For example:

```gherkin
Feature: User Authentication

Scenario: Successful login
  When I visit the login page
  And I enter "user@example.com" into the email field
  And I enter "some_password" into the password field
  And I click the login button
  Then I should be redirected to the dashboard
```

### 3. Install Syntestio

Follow the installation instructions at [https://syntestio.com/doc/install-package](https://syntestio.com/doc/install-package) to install the Syntestio tool.

### 4. Run your tests

Execute your tests using the Syntestio CLI:

```bash
syn --config path/to/your/config.json
```

For more detailed instructions on running tests, visit [https://syntestio.com/doc/run-tests](https://syntestio.com/doc/run-tests).

## Documentation

For complete documentation on Syntestio, please refer to the [Quickstart Guide](https://syntestio.com/doc/quickstart).
