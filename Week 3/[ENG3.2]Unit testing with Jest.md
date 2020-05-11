# Unit Testing with Jest

This lesson explains the basics of unit testing, examples of unit testing with Jest and a practice exercise writing unit tests

## Learning objectives

* TNTs will understand what unit testing is and why it's important
* TNTs will understand red, green, refactor pattern
* TNTs will understand Jest
* TNTs will write unit tests

## Time required and pace

Total time: 1.25 hour

* 15 minutes – What is unit testing? Why is it important in the software development lifecycle?
* 15 minutes – Red, Green, Refactor
* 15 minutes - Jest
* 30 minutes - Write unit tests

## Lesson details

### What is Unit Testing? And why? (15 minutes)

* Explain basic definition of unit testing
* What's the difference between unit test, integration test, functional test
* Perform unit testing in conjuction with feature implementation

Benefits of unit tests:

* Confidence in updating code - As a new developer on a team if you make changes to a module and all the unit tests pass you can have that much more confidence in not introducing bugs
* Reliable modules - A modules inputs can be tested with each unit test serving as a different scenario
* Reusability - An indirect benefit to writing your module to be "testable" results in smaller units of code with, ideally, one singular responsibilty
* Debugging is simpler - When searching for root cause of a defect you simply identify the module with a failing test. If there are no failing tests then that means there's a missing unit test ready to be written!

### Red, Green, Refactor (15 minutes)

Red, Green, Refactor is an engineering pattern of TDD (Test Driven Development) that is an effective way of writing unit tests.

1. Design a test by creating test scenarios (sometimes referred to as test cases)
2. Write a failing test (Red)
3. Write code to make the test pass (Green)
4. Refactor the code
5. Re-run the test to make sure it still passes

### Jest (15 minutes)

* Using Matchers - When testing values Jest provides "matchers" to help compare values
* Setup and Teardown - If you have code that needs to execute before or after many tests you can use beforeEach() and afterEach()
* Mocking - If your class depends on external classes mockinging can help to test behavior specific to your class only
* Async Code - Jest provides several ways to wait for async code to finish before proceeding to the next test

To install Jest:

1. npm install --save-dev jest
2. To write tests with Typescript we must install ts-jest using 'npm install --save-dev ts-jest @types/jest'
3. Create a jest config file using 'npx ts-jest config:init'

To run tests with Jest:

1. In the Terminal window use 'npm t'

### Let's write unit tests (30 minutes)

#### Examples of unit tests

This test will always pass

    test('a very simple test', () => {
        expect(true).toBe(true)
    })

Testing if a list contains an object

    const productList = [
        'Microsoft Surface Pro', 
        'Microsoft Office 365', 
        'XBox'
    ]

    test('the list of products contains Xbox', () => {
        expect(productList).toContain('Xbox')
    })

#### Practice writing unit tests

A starter project has been created which contains stubbed unit tests. Use the Red, Green, Refactor pattern to write some unit tests.

1. 'git clone' the TNT_Samples github repo <https://github.com/microsoft/TNT_Samples>
2. Use VS Code to open the 'Week_3/unit-testing-with-jest' project
3. Cmd+J to reveal the Terminal in VS Code
4. 'jest' and 'ts-jest' are already listed as dependencies in package.json so in the Terminal window type 'npm install' to install both dependencies
5. To run tests type 'npm t' in the Terminal window
6. The file src/store-locator/StoreFilter.test.tsx has empty test stubs that NT's will complete
