# Using Mocks
When unit testing it is important to use mocks for other functionality for classes. This makes sure that the test is only testing the functionality for that one class and not the functionality of other classes. It also helps to reinforce the single responsibility principle by emphasizing separation of concerns. An additional benefit is that if there are changes to other classes, the unit test for the desired class will not break.
  - ie. If testing class Alpha in your project and class Alpha calls a function from class Beta, class Alpha's instance of         class beta should be mocked out, and class Beta should have its own unit test for that function
    
# Integration Testing
Integration tests are used to test the full flow of an application and to make sure that all the components of work together properly. The goal of integration tests are to test that the full flow of an application works. This means that integration tests should usually just test the base cases of an application. As a result, most applications will have a large amount of unit tests, and a significantly smaller amount of integration tests.

Integration Test Workflow:
  1) Create database
  2) Load Data
  3) Run Test
  4) Retrieve Data
  5) Assert
  6) Rollback changes from test 
  7) Go to c if more tests or destroy db if no more tests

# Pair Programming
Pair programming is the act of two programers simultaniously working together on a single peace of code. During pair programming, there is one Driver and one Observer. The Driver is the one in control of the mouse and keyboard and actually doing the programming. The Observer observes the drivers programming and gives input/help. It is sugguested to rotate frequently when using pair programming in order to keep both developers involved. 
 
 Here is an example of a pair programming workflow using TDD
   1) Developer A writes a unit test for a needed piece of functionality
   2) Developer B writes the code that passes that piece of functionality
   3) Developer B then writes a unit test for another piece of functionality
   4) Developer A writes the code that passes that piece of functionality
   5) Reapeat 1-4 as for duration of pair programming
   
Studies have shown that pair programming produces code at a rate 15% lower then solo programming. However, pair programming also eliminates mistakes and reworks at a much higher rate and therefore ends up saving time overall.
