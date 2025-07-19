# Allure 3 Demo Project

## 📋 Prerequisites

- **Node.js** (v18 or higher)
- **pnpm** (v8 or higher) - Install via `npm install -g pnpm`
- **Operating System**: macOS, Linux, or Windows

## 🚀 Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd allure3-demo
```

2. Install dependencies:
```bash
pnpm install
```

3. Install Playwright browsers (required for E2E tests):
```bash
pnpm exec playwright install
```

## 🏃 Quick Start

### Run all tests and generate reports:
```bash
pnpm test
```

### View the generated reports:
```bash
pnpm report:open
```

That's it! Your browser will open with the Allure reports showing test results from both E2E and unit tests.

## 📖 Detailed Usage

### Running Specific Test Types

#### E2E Tests Only
```bash
pnpm test:e2e
```
Runs Playwright tests against https://allurereport.org across Chrome, Firefox, and Safari.

#### Unit Tests Only
```bash
pnpm test:unit
```
Runs Vitest unit tests demonstrating various test statuses and attachment handling.

#### Import Allure 2 Demo Data
```bash
pnpm test:allure2
```
Copies pre-existing Allure 2 test results for comparison and testing purposes.

### Test Execution Flow

1. **Clean Phase**: Removes previous test results automatically
2. **Test Phase**: Runs tests in parallel using `npm-run-all2`
3. **Report Phase**: Generates multiple report formats in `./allure-report/`
4. **History Phase**: Updates `history.jsonl` with execution data

## 📁 Project Structure

```
allure3-demo/
├── test/
│   ├── e2e/                    # Playwright E2E tests
│   │   ├── home.test.ts       # Homepage tests
│   │   ├── start.test.ts      # Getting started tests
│   │   └── pageObjects/       # Page Object Model
│   │       ├── common.ts
│   │       ├── home.ts
│   │       └── start.ts
│   └── unit/                   # Vitest unit tests
│       ├── index.test.ts      # Main unit tests
│       └── fixtures/          # Test assets
│           ├── image.jpg
│           ├── video.mp4
│           └── sample.*       # Code samples
├── allure-results/            # Test results (auto-generated)
├── allure-report/             # Generated reports
│   ├── awesomeAll/
│   ├── classic/
│   ├── dashboard/
│   └── csv/
├── allurerc.mjs              # Allure configuration
├── playwright.config.ts       # Playwright configuration
└── vitest.config.ts          # Vitest configuration
```

## 📚 Resources

- [Allure Documentation](https://allurereport.org/docs/)
- [Playwright Documentation](https://playwright.dev/)
- [Vitest Documentation](https://vitest.dev/)
