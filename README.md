# 🎯 Quiz Game -- Manual Testing Portfolio

A structured manual testing project for a **C-based console Quiz Game**,
covering menu navigation, topic selection, scoring logic, result
persistence, file handling, invalid inputs, boundary and security
scenarios, help and feedback flows, quit behavior, replay functionality,
and end-to-end testing.

The project includes **35 manually executed test cases** across
functional, positive, negative, scoring, boundary, file-handling,
input-validation, navigation, and end-to-end scenarios.

## 📌 Project Overview

The Quiz Game is a console application developed in C. Users can:

-   Start a quiz from the main menu
-   Choose from five quiz topics
-   Answer 10 multiple-choice questions per topic
-   Receive feedback for correct and incorrect answers
-   View the final score
-   Save and retrieve quiz results from a file
-   Read instructions and help information
-   Submit feedback
-   Replay another topic after completing a quiz
-   Quit or return to the main menu

### Available Quiz Topics

1.  Mathematics
2.  Physics
3.  Chemistry
4.  C Programming
5.  General Knowledge

------------------------------------------------------------------------

## 🧪 Test Execution Summary

  Metric                                Result
  ------------------- ------------------------
  Total Test Cases                          35
  Passed                                    32
  Failed                                     3
  Pass Rate                              91.4%
  Fail Rate                               8.6%
  Execution Status                   Completed
  Priority Coverage     Critical, High, Medium

### Overall Result

**32 of 35 test cases passed**, resulting in a **91.4% pass rate**.

Core quiz functionality---including topic selection, scoring, score
boundaries, result saving, replay, help, instructions, and most
invalid-input scenarios---worked successfully.

Three failed test cases identified issues in:

-   Invalid main-menu input handling
-   Missing result-file handling
-   Application quit behavior

------------------------------------------------------------------------

## 📊 Test Results by Module

  Module                      Total   Passed   Failed
  ------------------------ -------- -------- --------
  Main Menu                       4        3        1
  Topic Selection                 8        8        0
  Quiz & Scoring                  7        7        0
  Nickname Validation             3        3        0
  Result & File Handling          4        3        1
  Post-Quiz Navigation            3        3        0
  Help & Feedback                 2        2        0
  Quit Flow                       2        1        1
  Instructions                    1        1        0
  End-to-End                      1        1        0
  **Total**                  **35**   **32**    **3**

------------------------------------------------------------------------

## ❌ Failed Test Cases

  -----------------------------------------------------------------------
  Test Case ID      Scenario          Priority          Result
  ----------------- ----------------- ----------------- -----------------
  TC-MENU-04        Invalid main menu High              Fail
                    option                              

  TC-RESULT-03      View result when  Critical          Fail
                    result file is                      
                    missing                             

  TC-QUIT-01        Confirm           High              Fail
                    application quit                    
  -----------------------------------------------------------------------

### Key Risk Areas

#### 1. Invalid Main Menu Input Handling

The application should display an error and keep the menu stable after
unsupported input. The failed execution indicates that the
invalid-choice flow needs improvement.

#### 2. Missing Result File Handling

This is the highest-risk issue found during testing. When the result
file is unavailable, the application should detect the file-open failure
and show a clear message instead of attempting to read an invalid file
pointer.

#### 3. Quit Flow Reliability

The quit confirmation flow did not meet the expected behavior. The
application should terminate cleanly and consistently when the user
confirms exit.

------------------------------------------------------------------------

## 🧭 Main Menu Testing

The main menu was tested with:

-   Uppercase `S`
-   Lowercase `s`
-   Valid navigation options
-   Invalid character input

### Result

-   Uppercase start command: Pass
-   Lowercase start command: Pass
-   Menu options display: Pass
-   Invalid option handling: Fail

**Module Result: 3/4 Passed**

------------------------------------------------------------------------

## 📚 Topic Selection Testing

All available topic-selection paths were tested.

  Topic / Action               Result
  ---------------------------- --------
  Mathematics                  Pass
  Physics                      Pass
  Chemistry                    Pass
  C Programming                Pass
  General Knowledge            Pass
  Return to Home Page          Pass
  Unsupported Numeric Option   Pass
  Non-Numeric Topic Input      Pass

**Module Result: 8/8 Passed**

------------------------------------------------------------------------

## 🧮 Quiz & Scoring Testing

The scoring engine was tested using positive, negative, boundary, and
invalid-input scenarios.

### Scenarios Covered

-   Correct answer increases score by 1
-   Wrong answer does not increase score
-   All 10 correct answers produce a score of 10
-   All 10 wrong answers produce a score of 0
-   Uppercase answer input
-   Invalid answer character
-   Multi-character answer input

**Module Result: 7/7 Passed**

The score-boundary tests confirm that the application correctly handled
both minimum and maximum quiz scores during the executed scenarios.

------------------------------------------------------------------------

## 👤 Nickname Input Testing

Nickname handling was tested with:

-   Valid nickname
-   Blank nickname
-   Overlong nickname of more than 40 characters

All three executed scenarios passed according to the recorded test
results.

**Module Result: 3/3 Passed**

------------------------------------------------------------------------

## 💾 Result & File Handling Testing

The result module was tested for:

-   Saving the final score
-   Viewing a saved score
-   Missing result-file behavior
-   Latest result after completing multiple quizzes

  Scenario                Result
  ----------------------- --------
  Save final score        Pass
  View saved result       Pass
  Missing result file     Fail
  Latest score behavior   Pass

**Module Result: 3/4 Passed**

The missing-file scenario should be fixed before the application is
considered fully reliable because file operations require defensive
error handling.

------------------------------------------------------------------------

## 🔄 Post-Quiz Navigation & Replay

The application was tested after quiz completion for:

-   Returning to the Home Page
-   Starting another quiz topic
-   Entering an invalid post-quiz menu option

All tested scenarios passed.

**Module Result: 3/3 Passed**

------------------------------------------------------------------------

## 🆘 Help, Feedback & Instructions

Testing covered:

-   Opening usage help
-   Entering multi-word feedback
-   Opening instructions
-   Starting the game from the instructions screen

All recorded tests passed.

------------------------------------------------------------------------

## 🚪 Quit Flow Testing

  Scenario       Result
  -------------- --------
  Confirm Quit   Fail
  Cancel Quit    Pass

**Module Result: 1/2 Passed**

The application should be updated so that confirming the quit action
reliably terminates the program.

------------------------------------------------------------------------

## 🔁 End-to-End Testing

A complete user journey was tested:

1.  Launch the application
2.  Start the quiz
3.  Select a topic
4.  Answer all 10 questions
5.  View the result
6.  Select replay
7.  Return to topic selection
8.  Start another quiz flow

The complete end-to-end flow passed successfully.

**End-to-End Result: Pass**

------------------------------------------------------------------------

## 🧠 Test Design Techniques Applied

-   Functional Testing
-   Positive Testing
-   Negative Testing
-   Input Validation Testing
-   Boundary Value Testing
-   Scoring Validation
-   State Transition Testing
-   File Handling Testing
-   Navigation Testing
-   Security-Oriented Input Testing
-   End-to-End Testing
-   Error Handling Validation

------------------------------------------------------------------------

## 🛠️ Technology & Testing Environment

  Category               Technology
  ---------------------- -----------------------
  Application Type       Console Application
  Programming Language   C
  Testing Type           Manual Testing
  Test Documentation     Structured Test Cases
  Result Storage         Text File
  Platform               Windows Console
  Version Control        Git
  Repository Hosting     GitHub

------------------------------------------------------------------------

## 📂 Suggested Repository Structure

``` text
Quiz-Game/
│
├── quiz_game.c
├── README.md
├── testing/
│   └── Quiz_Game_Manual_Test_Cases.docx
└── screenshots/
    ├── passed-tests/
    └── failed-tests/
```

To link the complete test report from the repository:

``` md
[View Complete Manual Test Report](./testing/Quiz_Game_Manual_Test_Cases.docx)
```

------------------------------------------------------------------------

## 🚦 QA Assessment

### Strengths

-   All five quiz topics are accessible
-   Core scoring logic passed the executed tests
-   Minimum and maximum score boundaries worked correctly
-   Topic navigation is stable
-   Result saving and normal result retrieval work
-   Replay and post-quiz navigation work successfully
-   Help, feedback, and instruction flows passed
-   Complete end-to-end replay flow passed
-   Overall pass rate is 91.4%

### Areas for Improvement

-   Improve invalid main-menu input handling
-   Add safe error handling when the result file does not exist
-   Fix the quit-confirmation flow
-   Regression-test all three failed scenarios after fixes

### Recommendation

**Conditional GO / Fix Before Release**

The application demonstrates strong core functionality with a **91.4%
test pass rate**. However, the missing result-file failure is Critical,
and the menu-validation and quit-flow issues should also be fixed and
regression-tested before production release.

------------------------------------------------------------------------

## 👤 Author

### Masuduzzaman Niloy

**Software Quality Assurance (SQA) Enthusiast**

Focused on Manual Testing, API Testing, Database Testing, Test Case
Design, Defect Reporting, and Test Automation.

------------------------------------------------------------------------

⭐ This repository demonstrates practical manual testing skills through
structured test design, execution, scoring validation, invalid-input
testing, file-handling checks, and end-to-end QA assessment of a C-based
Quiz Game.
