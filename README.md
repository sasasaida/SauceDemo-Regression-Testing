# SauceDemo Regression Testing with Selenium

A browser automation project that records, organizes, and executes regression test cases for the [SauceDemo](https://www.saucedemo.com/) web application using Selenium IDE, Selenium WebDriver, and Python.

## Project Overview

This project demonstrates how Selenium IDE can be used to record browser interactions, organize test cases into a test suite, and export the recorded tests as an executable Python WebDriver script.

The tests cover login functionality and shopping cart operations.

## Test Scenarios

| Test ID | Test Case                             | Expected Result                                  |
| ------- | ------------------------------------- | ------------------------------------------------ |
| TC01    | Successful login with a standard user | User successfully reaches the inventory page     |
| TC02    | Login with a locked-out user          | Appropriate account-locked error message appears |
| TC03    | Add an inventory item to the cart     | Cart badge displays the correct item count       |
| TC04    | Remove an item from the cart          | Cart item is removed and the badge disappears    |

## Technologies Used

- Python 3.10+
- Selenium IDE
- Selenium WebDriver
- pytest
- Google Chrome
- SauceDemo demo web application

## Repository Structure

```text
SauceDemo-Regression-Testing/
│
├── SauceDemo_Regression_Project.side
├── test_sauceDemoRegressionSuite.py
├── requirements.txt
├── README.md
├── .gitignore

```

## Prerequisites

Before running the Python tests, install:

1. Python 3.10 or later.
2. Google Chrome browser.
3. Git (if cloning the repository).

Selenium Manager can automatically manage the required browser driver in supported Selenium versions.

**Note:** Selenium IDE is only needed if you want to open, inspect, or modify the recorded `.side` project. It is not required to execute the exported Python tests.

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/SauceDemo-Regression-Testing.git
```

Navigate into the project directory:

```bash
cd SauceDemo-Regression-Testing
```

### 2. Create a virtual environment

**Windows:**

```bash
python -m venv .venv
```

Activate it:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 4. Run the regression test suite

Make sure Google Chrome is installed and then execute:

```bash
python -m pytest -v test_sauceDemoRegressionSuite.py
```

pytest will execute the four test cases and display whether each test passed or failed.

## Test Application Credentials

The tests use the publicly available SauceDemo demonstration accounts.

| Account         | Username          | Password       |
| --------------- | ----------------- | -------------- |
| Standard user   | `standard_user`   | `secret_sauce` |
| Locked-out user | `locked_out_user` | `secret_sauce` |

Application URL: https://www.saucedemo.com/

These are demonstration credentials, not private account credentials.

## Selenium IDE Project

The file `SauceDemo_Regression_Project.side` contains the recorded Selenium IDE project and the `SauceDemo_Regression_Suite` test suite.

To inspect or edit it:

1. Install the Selenium IDE browser extension.
2. Open Selenium IDE.
3. Import the `.side` project file.
4. Select the regression test suite.
5. Run the individual tests or the complete suite.

## Assertions and Locators

The project demonstrates Selenium IDE commands and browser element locators, including:

- `assertText`
- `assertElementPresent`
- `assertElementNotPresent`
- `verifyValue`
- ID locators
- CSS selectors

The exported Python script uses Selenium WebDriver to locate elements, interact with the browser, and verify expected results.

## Test Results

The tests should be run against the live SauceDemo demonstration application. Actual execution results depend on the availability of the application, browser, and test environment.

Screenshots of the recorded test cases and successful test execution can be found in the `screenshots/` directory, when included.

## Notes

- The tests use the public SauceDemo demonstration application.
- Each test should establish the application state it needs instead of relying on a previous test's browser state.
- The Python dependencies are listed in `requirements.txt`.
- The virtual environment and generated cache files are intentionally excluded from version control.

## Author

**Saida Jahan**

Software Testing and Maintenance Laboratory Project

GitHub: https://github.com/sasasaida
