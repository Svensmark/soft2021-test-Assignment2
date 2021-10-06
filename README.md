# Emil Svensmark - Assignment 2, 06-10-2021
# 1 REFLECTIONS
## 1.1 Computer Mouse
### Identify the types of testing you would perform on a computer mouse, to make sure  that it is of the highest quality.
1. Functional testing (unit testing of each input button on mouse aswell as sensors).
2. Load testing/Stress testing (physical stress).

## 1.2 Catastrophic failure
### Find a story where a software system defect had a bad outcome. Describe what happened. Can you identify a test that would have prevented it? 

https://www.wired.com/2010/11/1110mars-climate-observer-report/

In 1999 a Mars Climate Orbitor burned up in the Martian atmosphere due a simple software failure. In the link above an article is written about the whole disaster.

"[..] The software calculated the force the thrusters needed to exert in pounds of force. A separate piece of software took in the data assuming it was in the metric unit: newtons. "

My suggestion to a test to this specific problem, would be a *unit test*. The reason for this would be, as it explained in the article, it was a piece of a software, which makes me assume it was a *unit* of the software, which would make unit testing a great solution. 

#
# 2 TWO KATAS 
### Complete the following using TDD. Remember the TDD mantra.
## 2.1 STRING UTILITY
### Use TDD to create a string utility with the following methods:
1. Reverse string (aBc -> cBa) - **(Implemented in project.)**
1. Capitalize string (aBc -> ABC) - **(Implemented in project.)**
1. Lowercase string (aBc -> abc)   - **(Implemented in project.)**

Don’t use any built-in string utility – create your own. Remember, the exercise here is to 
use TDD, not to deliver a working utility without tests. If there are no tests in the 
solution, it won’t be accepted.

## 2.2 Bowling game kata
### I can't view the powerpoint, so i can't solve this task.

#
# 3 Investigation of tools 
## 3.1 JUnit 5
### Investigate JUnit 5 (Jupiter). Explain the following, and how they are useful.
1. @Tag - Used for filtering tests to certain environments, for example production and development tests can be seperated and run seperately with @IncludeTags.
2. @Disabled - Used to disable a certain test, which is useful for when you don't wish for the certain test to run.
3. @RepeatedTest - Used to repeat the same test a multitude of times. Useful for when you wish a test to be run multiple times.
4. @BeforeEach, @AfterEach - Used to call functions or initialize values/objectes before and/or after each test is run. This is useful for when you want to clear a database that has been used in a previous test, for example.
5. @BeforeAll, @AfterAll - Used to call functions or initialize values/objects before and/or after every test is run (not to be confused with Before/AfterEach that is run after every single test). Usuful to setup test environment before tests and break it down again after tests has been run.
6. @DisplayName - DisplayName is used to give a test class a custom name that will be printed in the IDE test report. Its useful information that makes the test report give more information.
7. @Nested - Is a way to create a nested test class within another test class. 
8. assumeFalse, assumeTrue - After the assume function is called, if the outcome is true then the test will continue to execute, otherwise it will skip the entire test.