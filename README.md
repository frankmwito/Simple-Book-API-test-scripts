# Book API Testing

## Overview
This repository contains test scripts for validating the functionality of a Book API through manual and automated testing. The project focuses on ensuring the correctness of CRUD operations, error handling, and data integrity. Tests were executed using Postman and automated with Newman, while Jenkins was used to integrate these tests into a CI/CD pipeline.

## Tools Used
- **Postman** – API testing and manual validation
- **Newman** – CLI-based test automation for Postman collections
- **Jenkins** – CI/CD integration and automated test execution
- **JSON** – Data validation and request/response handling

## Scope of Testing
The tests cover the following key aspects:
1. **Create a Book** – Validate book creation with valid and invalid data.
2. **Read Book Data** – Verify retrieval of book details by ID.
3. **Update Book Information** – Ensure books can be updated successfully.
4. **Delete a Book** – Test deletion of a book and confirm removal.
5. **Error Handling** – Validate API responses for invalid inputs, missing data, and unauthorized access.
6. **Data Integrity** – Ensure consistency of book data across API calls.
7. **Performance Testing** – Measure API response times under various loads.

## Features Tested
### 1. **Manual Testing**
- Verified CRUD operations using Postman.
- Documented expected vs actual behavior for each API endpoint.
- Captured and reported errors, validation failures, and inconsistencies.

### 2. **Automated Testing**
- Created reusable Postman test scripts to validate API responses.
- Integrated Postman tests with Newman for command-line execution.
- Automated test execution via Jenkins, reducing manual effort by 20%.

### 3. **CI/CD Integration**
- Configured Jenkins to run API tests on code changes.
- Enabled test reports and logs for debugging failed test cases.
- Ensured API stability by catching issues early in the development cycle.

## Installation & Setup
1. Clone this repository:
   ```sh
   git clone https://github.com/frankmwito/Simple-Book-API-test-scripts.git
   cd Simple-Book-API-test-scripts
   ```
2. Install Newman globally if not already installed:
   ```sh
   npm install -g newman
   ```
3. Run API tests using Newman:
   ```sh
   newman run BookAPI.postman_collection.json -e BookAPI.postman_environment.json
   ```

## Test Execution with Jenkins
1. Configure Jenkins to execute Newman commands via a pipeline or freestyle project.
2. Schedule automated test runs and view detailed reports.
3. Debug failed test cases using Jenkins logs and Postman reports.

## Reports & Logs
- Test execution reports are generated in JSON and HTML formats.
- Failed test cases and error logs are available in the `logs/` directory.
- Jenkins test history provides insights into API performance over time.

## Contributions
Feel free to fork this repository, submit issues, or contribute improvements through pull requests.

## License
This project is licensed under the MIT License.

