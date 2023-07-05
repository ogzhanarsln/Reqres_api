Reqres Test API Automation

This repository contains API automation tests for the Reqres Test project. The tests are designed to validate the functionality, security, and performance of the Reqres API endpoints. This README file provides instructions on how to import and run the tests in Postman.

Getting Started

Prerequisites
To run the API tests, you need to have the following installed:
- [Postman](https://www.postman.com/downloads/) - a collaboration platform for API development and testing.

Importing the Tests
1. Clone or download this repository to your local machine.
2. Open Postman and click on the "Import" button in the top-left corner.
3. In the import modal, select the "Folder" tab.
4. Click on "Choose Folder" and browse to the location where you cloned/downloaded this repository.
5. Select the folder containing the test collection and environment files.
6. Click on "Import" to import the tests into Postman.

Setting Up the Environment
1. In Postman, click on the "Manage Environments" button (gear icon) on the top-right corner.
2. Click on "Import" and browse to the location where you cloned/downloaded this repository.
3. Select the environment file (`Reqres Environment.postman_environment.json`) and click on "Open" to import it.
4. Once imported, select the imported environment from the drop-down menu to activate it.

Running the Tests
1. In Postman, locate the imported collection in the left sidebar.
2. Click on the collection to expand it and view the available test scenarios.
3. Click on the specific test scenario you want to run.
4. Click on the "Send" button to send the request and execute the test.
5. The test results will be displayed in the "Tests" tab of the Postman interface.

Test Scenarios
The API tests cover the following scenarios:
- Register Successful (POST)
- Register Unsuccessful (POST)
- Login Successful (POST)
- Login Unsuccessful (POST)
- Logout (POST)
- Update (PUT)
- Update Unsuccessful (PUT)
- Delete (DELETE)
- Delete Unsuccessful (DELETE)

Each test scenario is designed to validate specific functionalities and handle both successful and unsuccessful scenarios.

Bugs
The following bugs have been identified in the Reqres Test API:

1. Update Unsuccessful (PUT)
   - Description: The "name" field should only accept a string value, but the API allows updating it to an integer value without returning an appropriate error response.
   - Expected Behavior: When a user updates the "name" field to an integer value, the response should be 400.
   - Actual Behavior: The response returns 200 instead of 400.

2. Delete Unsuccessful (DELETE)
   - Description: When sending a DELETE request with an unavailable user ID in the URL, the API should return a 404 response to indicate that the user does not exist. However, the API returns a 200 response instead.
   - Expected Behavior: When the URL contains an unavailable user ID, the response should be 404.
   - Actual Behavior: The response returns 200 instead of 404.

Conclusion
The API automation tests in this repository are designed to validate the functionality, security, and performance of the Reqres Test project. By following the instructions provided, you can import and run these tests in Postman. The identified bugs can serve as starting points for further investigation and improvements to the API.