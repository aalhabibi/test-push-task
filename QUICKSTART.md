# Quick Start Guide

## What's been set up

Your project now has:
- ✅ Calculator class with basic operations
- ✅ Comprehensive JUnit 5 tests (6 test cases)
- ✅ Maven build configuration
- ✅ GitHub Actions workflow for automated testing on push
- ✅ All tests passing locally

## Project Structure

```
test-push-task/
├── .github/
│   └── workflows/
│       └── maven-test.yml          # Runs tests automatically on push
├── src/
│   ├── main/java/
│   │   ├── App.java                # Main application
│   │   └── Calculator.java         # Calculator with operations
│   └── test/java/
│       └── CalculatorTest.java     # JUnit test cases
├── pom.xml                          # Maven configuration
├── .gitignore                       # Ignores build artifacts
└── README.md                        # Full documentation
```

## Next Steps

### 1. Initialize Git Repository (if not already done)
```bash
git init
git add .
git commit -m "Initial commit: Java project with tests and CI/CD"
```

### 2. Create GitHub Repository
1. Go to GitHub.com
2. Create a new repository (don't initialize with README)
3. Push your code:
```bash
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
git branch -M main
git push -u origin main
```

### 3. Watch the Tests Run!
- Go to your repository on GitHub
- Click the "Actions" tab
- You'll see the workflow running automatically
- Tests will run every time you push code

## Testing Locally

```bash
# Run tests
mvn test

# Run the application
mvn compile exec:java -Dexec.mainClass="App"

# Build JAR
mvn package
java -jar target/test-push-task-1.0-SNAPSHOT.jar
```

## What Happens on Push?

When you push to GitHub, the workflow automatically:
1. ✅ Checks out your code
2. ✅ Sets up JDK 11
3. ✅ Builds the project
4. ✅ Runs all 6 test cases
5. ✅ Generates test reports
6. ✅ Uploads results as artifacts

## Test Coverage

Current tests verify:
- Addition (positive, negative, zero)
- Subtraction
- Multiplication
- Division (including divide-by-zero exception handling)
- Even number detection

All 6 tests are currently passing! ✨
