# IT23142978_ITPM_Assignment1
IT23142978_IT3040 _ITPM_Assignment_1

# SwiftTranslator Test Automation Suite

This project contains automated tests for the SwiftTranslator Singlish to Sinhala conversion system using Playwright.

## Project Overview

This test suite validates the functionality of the SwiftTranslator web application by testing:
- 24 positive functional scenarios
- 10 negative functional scenarios  
- 1 UI-related test scenario

## Prerequisites

Before running the tests, ensure you have the following installed:
- Node.js (version 16 or higher)
- npm (comes with Node.js)

## Installation

### Step 1: Clone or Download the Repository

If you have the project as a zip file, extract it. If it's a Git repository:

```bash
git clone <repository-url>
cd <project-directory>
```

### Step 2: Install Dependencies

Run the following command in the project root directory:

```bash
npm install
```

### Step 3: Install Playwright Browsers

After installing dependencies, install the required browsers:

```bash
npx playwright install chromium
```

## Project Structure

```
.
├── swift-translator-tests.spec.js    # Main test file
├── playwright.config.js              # Playwright configuration
├── package.json                      # Project dependencies
└── README.md                         # This file
```

## Running the Tests

### Run All Tests

```bash
npm test
```

### Run Tests in Headed Mode (visible browser)

```bash
npm run test:headed
```

### Run Tests with UI Mode (interactive)

```bash
npm run test:ui
```

### Run Tests in Debug Mode

```bash
npm run test:debug
```

### View Test Report

After running tests, view the HTML report:

```bash
npm run report
```

## Test Coverage

### Positive Functional Tests (24 scenarios)

The test suite covers:
- ** Simply short  question
- **  Simple request
- **Convert a short sentense with Units of measurements
- **Complex sinhala words
- **Frequently used day-to-day expressions, Slangs
- ** Imperative (commands) forms
- **Convert a short phrase with English brand terms
- **Negation patterns
- **Positive forms
- **Common greetings
- **Convert  request phrase
- **Request forms with varying degrees of politeness + Multiple spaces
- **responses with  punctuation marks
- **Informal phrasing
- **Frequently used day-to-day expressions
- **Multi-word expressions + frequent collocations
- **Repeated word expressions
- **past Tense variations
- **informal phrasing
- **Currency measurement + English short forms
- ** Slang and colloquial phrasing + english words that normally used 
- **English abbreviations+ Medium letters
- **Request forms with varying degrees of politeness + Multiple spaces
- **

### Negative Functional Tests (10 scenarios)
- **simple sentense with common English words + English  short forms
- **Convert a short request phrase
- **English mixed polite sentence
- **Random letters (no meaning)
- **Unsupported language (English sentence)
- **Mixed symbols and text
- **Misspelled Singlish word
- **Question with spacing error input
- **Complex slang statement with english words
- **capitaliezed words

### UI Test (1 scenario)

-Overflow handling

## Test Data Structure

Each test case includes:
- **Test Case ID**: Unique identifier (e.g., Pos_Fun_001)
- **Name**: Descriptive test name
- **Input**: Singlish text to translate
- **Expected Output**: Expected Sinhala translation


## Configuration

Test timeouts and settings can be modified in `playwright.config.js`:
- Default timeout: 60 seconds
- Expect timeout: 10 seconds
- Retries: 0 (can be increased for flaky tests)
- Workers: 1 (sequential execution)

## Troubleshooting

### Tests Failing

1. **Network Issues**: Ensure stable internet connection
2. **Site Changes**: Website structure may have changed - verify selectors
3. **Timeout Errors**: Increase timeout values in config or test files

### Installation Issues

1. **Node.js Version**: Ensure you're using Node.js 16+
   ```bash
   node --version
   ```

2. **Clear Cache**: If having npm issues
   ```bash
   npm cache clean --force
   npm install
   ```

### Browser Issues

If Playwright browsers aren't working:
```bash
npx playwright install --force chromium
```

## Test Results

Test results are saved in the `test-results/` directory:
- HTML report: `test-results/html-report/`
- JSON results: `test-results/test-results.json`
- Screenshots/Videos: `test-results/artifacts/`

## Notes

- Tests run sequentially (workers: 1) to avoid conflicts
- Each test waits 2 seconds between executions for stability
- Screenshots and videos are captured only on failure
- All tests use the same base URL configured in `playwright.config.js`

## License

This project is for educational purposes as part of IT3040 - ITPM assignment.

## Author

BSc (Hons) in Information Technology - Year 3 Student
