# Petstore API Tests

This repository contains automated tests for the Petstore API using Postman and Newman. The tests verify the functionality of adding and updating pets in the Petstore application. The tests can be run locally in Postman or as part of a CI/CD pipeline on GitHub.

## Table of Contents

- [Getting Started](#getting-started)
- [Running Tests in Postman](#running-tests-in-postman)
- [CI/CD with GitHub Actions](#cicd-with-github-actions)

## Getting Started

To get started with the Petstore API tests, you will need to have Postman installed for local testing. If you want to run the tests using CI/CD on GitHub, ensure you have access to a GitHub repository.

### Prerequisites

- [Postman](https://www.postman.com/downloads/) (for local execution)
- Node.js (for running Newman in CI/CD)

## Running Tests in Postman

1. **Import the Collection**:
   - Open Postman and click on the "Import" button.
   - Upload the `Petstore_Assignment.postman_collection.json` file from the repository.

2. **Set Environment Variables**:
   - Before running the tests, make sure to set the `baseUrl` variable in your Postman environment. 
   - **Value**: `https://petstore.swagger.io/v2`

3. **Run the Tests**:
   - Select the imported collection in Postman.
   - Click on the "Run" button to execute the tests.
   - View the results in the Postman console.

### Test Cases

- **Add a new pet to the store**
- **Update an existing pet**

Each test case verifies the response status code and specific field values in the response JSON.

## CI/CD with GitHub Actions

This repository is set up to run Postman tests automatically using GitHub Actions whenever changes are pushed to the `main` branch or a pull request is created.

### Steps Explained:

1. **Checkout repository**: Checks out the code from the repository.
2. **Install Node.js**: Sets up Node.js version 16 in the GitHub Actions environment.
3. **Install Newman**: Installs the Newman package globally to allow running Postman collections.
4. **Run Postman collection**: Executes the Postman collection using Newman. The results are exported in both CLI and JSON formats.

### Viewing Results:

After the tests run, you can view the results in the "Actions" tab of your GitHub repository. Each run will provide logs of the test execution and indicate whether the tests passed or failed.
