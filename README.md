# Slow test reporter for jest

No dependencies, no interactive shell needed.  Prints out the slowest 10 tests in your app.  Can also print warnings when a test exceeds X ms.

## Installation

You may install this package as a development dependency:

```bash
npm install --save-dev jest-slow-test-reporter
yarn add --dev jest-slow-test-reporter
```

## Configuration

Configure [Jest](https://facebook.github.io/jest/docs/en/configuration.html) to use the reporter.

For example, create a `jest.config.js` file containing:

```javascript
module.exports = {
  verbose: false,
  reporters: [
    ['jest-slow-test-reporter', {"numTests": 8, "warnOnSlowerThan": 300, "color": true}]
  ]
};
```

numTests controls how many slow tests to print.
warnOnSlowerThan will warn when a test exceeds this time in milliseconds.
color will make the warnOnSlowerThan warning messages print in red
