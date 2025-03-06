# Cucumber Demo Project Using Selenium with Java, Maven, and TestNG

This repository demonstrates a test automation framework that integrates **Behavior-Driven Development (BDD)** principles with the **Page Object Model (POM)** design pattern. The framework leverages **Selenium WebDriver** for browser automation, **Cucumber** for writing test scenarios in Gherkin, and **TestNG** for test execution, including support for parallel test runs. Built with **Maven** for project management, this Proof of Concept (POC) provides a scalable and maintainable foundation for automated testing.

---

## Prerequisites

Before setting up the project, ensure the following tools are installed on your system:

- **[Java Development Kit (JDK) 8 or higher](https://www.oracle.com/java/technologies/javase-downloads.html)**: Required to compile and run the Java-based framework.
- **[Maven](https://maven.apache.org/download.cgi)**: Used for dependency management and build automation.
- **An Integrated Development Environment (IDE)**: Recommended options include [IntelliJ IDEA](https://www.jetbrains.com/idea/download/) or [Eclipse](https://www.eclipse.org/downloads/).
- **A web browser**: Such as Chrome or Firefox, for test execution.
  
**Note**: This project uses [WebDriverManager](https://github.com/bonigarcia/webdrivermanager) to automatically manage WebDriver binaries (e.g., ChromeDriver, GeckoDriver), so manual setup of WebDriver executables is not required.

---

## Setup Instructions

Follow these steps to set up the project on your local machine:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-repo-url.git
   ```
   Replace `your-repo-url` with the actual repository URL.

2. **Open the project in your IDE**:
   Launch IntelliJ IDEA, Eclipse, or your preferred IDE and import the project as a Maven project.

3. **Download dependencies**:
   Allow the IDE to resolve Maven dependencies automatically. If necessary, run the following command in the terminal from the project root:
   ```bash
   mvn clean install
   ```
   This ensures all required libraries are downloaded and the project is built successfully.

---

## Running the Tests

To execute the test suite:

- **Using the IDE**:
  1. Navigate to `src/test/java/runners/TestRunner.java`.
  2. Right-click the file and select **"Run"** to execute the tests via TestNG.

- **Using the terminal**:
  Run the following Maven command from the project root:
  ```bash
  mvn clean test
  ```

This will trigger the Cucumber scenarios defined in the feature files, with TestNG managing the execution, including parallel test runs where configured.

---

## Project Structure

The framework is organized into the following key directories and components:

- **`src/main/resources/Features`**:
  Contains Cucumber feature files written in Gherkin. For this demo, the file `loginFeature2.feature` showcases a sample login scenario.

- **`src/test/java/stepDefinition`**:
  Houses step definition classes (e.g., `LoginPageStepDefinition.java`) that map Gherkin steps to executable Java code, implementing the test logic.

- **`src/test/java/pageObjects`**:
  Contains page object classes that encapsulate web page elements and interactions, adhering to the POM design pattern for better maintainability and reusability.

- **`src/test/java/runners`**:
  Includes the `TestRunner.java` class, which uses TestNG to configure and initiate Cucumber test execution, enabling features like parallel running.

- **`target/cucumber-reports`**:
  The directory where test execution reports are generated post-run.

The `pom.xml` file in the project root manages all dependencies and build configurations using Maven.

---

## Reporting

After running the tests, detailed HTML reports are generated in the `target/cucumber-reports` directory. To view the results:
1. Navigate to `target/cucumber-reports/index.html`.
2. Open the file in a web browser to explore the test outcomes, including pass/fail statuses and step-by-step execution details.

---

## Key Features

This framework highlights the following capabilities:

- **Behavior-Driven Development (BDD)**:
  Utilizes Cucumber and Gherkin to write tests that are readable by both technical and non-technical stakeholders.

- **Page Object Model (POM)**:
  Organizes code into page-specific classes, enhancing reusability and reducing maintenance effort.

- **Parallel Execution**:
  Leverages TestNG to run tests concurrently, optimizing execution time for larger test suites.

- **Automated Reporting**:
  Provides comprehensive HTML reports via Cucumber, offering clear insights into test results.

This POC serves as a starting point for building more complex and tailored test automation solutions.

---

Feel free to explore and adapt this demo project to meet your testing needs! For additional resources, refer to the documentation of the technologies used: [Selenium](https://www.selenium.dev/documentation/), [Cucumber](https://cucumber.io/docs/gherkin/), [TestNG](https://testng.org/doc/), and [Maven](https://maven.apache.org/guides/).

---
