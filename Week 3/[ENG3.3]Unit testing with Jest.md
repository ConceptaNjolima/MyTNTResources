# Unit Testing with Jest

This lesson explains the basics of unit testing and examples of unit testing with Jest.

## Learning objectives

* TNTs will understand what unit testing is and why it's important
* TNTs will understand red, green, refactor pattern
* TNTs will write basic unit tests

## Time required and pace

Total time: 1 hour

* 15 minutes – What is unit testing? Why is it important in the software development lifecycle?
* 15 minutes – Red, Green, Refactor
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

1. Design a test and it's test scenarios (sometimes referred to as test cases)
2. Write a failing test (Red)
3. Write code to make the test pass (Green)
4. Refactor the code
5. Re-run the test to make sure it still passes

### Let's write unit tests (30 minutes)
