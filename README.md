# Test Push Task - Java CI/CD Lab

A simple Java project demonstrating automated testing on push using GitHub Actions.

## Project Structure

```
.
├── .github/
│   └── workflows/
│       └── maven-test.yml    # GitHub Actions workflow
├── src/
│   ├── App.java              # Main application
│   ├── Calculator.java       # Calculator class with basic operations
│   └── CalculatorTest.java   # JUnit test cases
├── pom.xml                    # Maven configuration
└── README.md
```

## Features

- Simple Calculator class with basic operations (add, subtract, multiply, divide)
- Comprehensive JUnit 5 test cases
- Maven build configuration
- GitHub Actions CI/CD pipeline that runs tests on every push

## Running Locally

### Prerequisites

- Java 11 or higher
- Maven 3.6+

### Build the project

```bash
mvn clean compile
```

### Run tests

```bash
mvn test
```

### Run the application

```bash
mvn exec:java -Dexec.mainClass="App"
```

Or build and run the JAR:

```bash
mvn clean package
java -jar target/test-push-task-1.0-SNAPSHOT.jar
```

## GitHub Actions Workflow

The workflow (`.github/workflows/maven-test.yml`) automatically:

1. Checks out the code
2. Sets up JDK 11
3. Builds the project with Maven
4. Runs all test cases
5. Generates test reports
6. Uploads test results as artifacts

The workflow triggers on:

- Push to `main` or `master` branch
- Pull requests to `main` or `master` branch

## Test Coverage

The `CalculatorTest` class includes tests for:

- Addition (including negative numbers)
- Subtraction
- Multiplication
- Division (including divide by zero exception)
- Even number checking

## How to Use

1. Push your code to GitHub
2. GitHub Actions will automatically run the tests
3. Check the Actions tab in your repository to see test results
4. Test reports will be available as downloadable artifacts
