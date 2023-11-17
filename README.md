
# UcupTest
Simple API Test Framework

## Introduction


## Installation

Install Ucuptest from NPM into your project:

    npm i ucuptest-new

## Creating Tests

### Simple Example

The minimum setup to run a single test expectation.

```javascript
const { Ucuptest } = require('ucuptest-new');
const ucuptest = new Ucuptest();

ucuptest.setBaseUrl('https://jsonplaceholder.typicode.com'); // Ganti dengan base URL yang sesuai

ucuptest.get('/todos/1', {}, null, 'Simple Test')
  .then(responseData => {
    console.log(responseData)
  })
  .finally(() => {
    ucuptest.runTests();
  });

```