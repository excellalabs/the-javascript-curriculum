
> This document contains JavaScript Best Practies

#### Basics
> These are JavaScript basics to be aware of.

  1. `===` vs `==`
  
      ```javascript
      function incorrect() {
       var changeDue = "5.99";
       if (changeDue == 5.99) {
        return true;
       } else {
        return false;
       }
      }
      // output: false
      
      function correct() {
       var changeDue = "5.99";
       if (changeDue === 5.99) {
        return true;
       } else {
        return false;
       }
      }
      // output: true
      ```
      
  2. Lines of code per JS file
    
    ```
    At what point do we consider a JS file "too large"?
    ```
    
  3. `<head>` vs `<body>`
  
    ```
    True or False: It is good practice to put your scripts within the <head> tag of an HTML document.
    
    // output: False; browsers render pages more slowly when scripts are in the <head> tag (as opposed to <body>).
    ```

  4. `'` vs `"`
  
    ```
    Which of the following variable declarations will properly create a string in JavaScript?
    
    A) var message = "Choice A.";
    B) var message = 'Choice B.';
    C) Both A) and B) will properly create a string.
    
    // output: C); Single and double quotes both work fine, but it is best practice to choose one or the other for your project and stick to it.
    ```

  5. Formatting
      - Whitespace
        - 1) Whitespace between keywords/operators and parameters
        ```javascript
        if (condition) { ... }
        ```
        - 2) No whitespace
        ```javascript
        if(condition){ ... }
        ```
        - 1) is preferred for readability purposes. 
      - Curly bracket placement
        - 1) Inline placement
        ```javascript
        if (condition) {

        } else {
        
        }
        ```
        - 2) Line break placement
        ```javascript
        if (condition) 
        {
        
        }
        else 
        {
        
        }
        ```
        - 1) is good for reducing the number of lines in a file. 
        - 2) more explicitly separates function/conditional statement definitions.
        - Be consistent with whichever you choose.
      - Line breaks
        - No general rules of thumb here. Be conscious about breaking up consecutive
        lines of statements into logical chunks.
      - Semi-colons (yes or no?)
        - Pros of using semicolons: 
          - Consistent with popular languages
          - Promotes readability and writability if accustomed to languages that use them
        - Pros of omitting semicolons:
          - Less typing
        - Be consistent with whichever you choose.
  6. Shorthand expressions
    - Although they can make trivial statements more concise, beware of nesting complicated logic
    inside shorthands. You will sacrifice readability for concision.
    - Good example
    ```javascript
    // Original
    var biggerThanFive;
    if (x > 10) {
        biggerThanFive = 'Yes';
    } else {
        biggerThanFive = 'No';
    }
    
    // Shorthand
    var biggerThanFive = x > 10 ? 'Yes' : 'No';
    ```
    - Comprehensive list: https://www.sitepoint.com/shorthand-javascript-techniques/
  7. Variable declaration
    - Good practice (locally scoped):
    ```javascript
    var myObj = {};
    ```
    - Bad practice (unintentional global scope)
    ```javascript
    myObj = {};
    ```
  8. `that` vs `thisView` vs `self`
    - You will often need to declare a local copy of the current view for the
    sake of scoping:
    ```javascript
    function myFunction() {
        var thisView = this;

        var anotherFunction = function() {
            thisView.outsideFunction();
        };
    }
    ```
    - The name that you use for this copy is really a matter of preference,
    but to be more descriptive, thisView is usually a good choice for naming.
  9. Use of third-party libraries
    - Don't know what to put this for one. Does tethering your JS closely to
    third-party libraries introduce instability if the third parties change
    their interfaces eventually?

    - Or should you use third-party libraries to avoid reinventing the wheel
    everytime you want to do something relatively complex?
      
#### Worst Practices
> These are coding practices to avoid and habits that you should unlearn.

#### Obsolete Practices
> These are coding practices that were once good but have become dated and should be avoided.

  1. Overusing jQuery
      
      Most modern applications use jQuery as an ancillary library, opting for a js framework with features that jQuery doesn't provide (data-binding, routing, etc.) as the primary front-end framework. As such, methods and functions provided by the primary framework should be used before jQuery usage is considered.  Additionally:
      -  Avoid making duplicate jQuery calls.  Instead, store the result of the initial call in a variable. 
      
      
      Bad Practice
      ```javascript
      $('.descriptionDiv').find('').val();
      ```
     
      
     Good Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```
      
      -  Ensure that the most efficient jQuery call is used
      
      
      
      Bad Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```
     
      
     Good Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```
  2. Relying on Comments to Clarify Overly Complex or Confusing Code
      
      
      
      
      Bad Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```
     
      
     Good Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```
  3. Storing JavaScript Code in One File
      
      Here's where the explanation goes.
     
  4. Manipulating Globals
      
      Here's where the explanation goes.
      
      
      Bad Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```
     
      
     Good Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```
  5. Manipulating Prototypes (manually or in frameworks like date.js)
      
      Here's where the explanation goes.
      
      
      Bad Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```
     
      
     Good Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```
  6. Using Browser Detection Instead of Feature Detection
      
      Here's where the explanation goes.
      
      
      Bad Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```
     
      
     Good Practice
      ```javascript
      function test() {
       console.log("look ma`, no spaces");
      }
      ```

#### Good Practices
> Universally applicaple and common sense coding and software development practices.

Lorem ipsum

#### Agile Engineering 
> These are Agile Engineering best practices

  1. Test Driven Development (TDD)
    
    **Why should you do it?** Because it's awesome.
    1. Unit Testing
    
    Lorem ipsum
    > **Recommended Tool** `jasmine`
  1. SOLID
  
  Lorem ipsum
  1. Clean Code
  
  Lorem ipsum
  
#### Industry Practices
> Here are some notable examples of what successful tech companies use and do. Pick what best works for you.

Lorem ipsum 

#### Tooling
> These are easy to learn and use tools.

Lorem ipsum
