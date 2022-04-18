# pytest
The pytest framework makes it easy to write small, readable tests, and can scale to support complex functional testing for applications and libraries.

If you’ve written unit tests for your Python code before, then you may have used Python’s built-in unittest module. unittest provides a solid base on which to build your test suite, but it has a few shortcomings.

A number of third-party testing frameworks attempt to address some of the issues with unittest, and pytest has proven to be one of the most popular. pytest is a feature-rich, plugin-based ecosystem for testing your Python code.

pytest simplifies this workflow by allowing you to use Python’s assert keyword directly

That’s it. You don’t have to deal with any imports or classes. Because you can use the assert keyword, you don’t need to learn or remember all the different self.assert* methods in unittest, either. If you can write an expression that you expect to evaluate to True, then pytest will test it for you. You can run it using the pytest command:

## Installation:
> pytest will run any python file  of the form test_*.py or *_test.py in the current directory and its subdirectories. More generally, it follows standard test discovery rules.

    pip install -U pytest


    # content of test_sample.py
        def func(x):
         return x + 1


        def test_answer():
         assert func(3) == 5

- to try the test type in the terminal or cmd:
    
        pytest


    ================== test session starts =============================
    platform darwin -- Python 3.7.3, pytest-5.3.0, py-1.8.0, pluggy-0.13.0
    rootdir: /.../effective-python-testing-with-pytest
    collected 2 items

    test_with_pytest.py .F                                          [100%]

    ======================== FAILURES ==================================
    ___________________ test_always_fails __________________________

            def test_always_fails():
                assert False
                assert False

    test_with_pytest.py:5: AssertionError
    ============== 1 failed, 1 passed in 0.07s =========================

---
- pytest presents the test results differently than unittest. The report shows:

- The system state, including which versions of Python, pytest, and any plugins you have installed
- The rootdir, or the directory to search under for configuration and tests
- The number of tests the runner discovered
- The output then indicates the status of each test using a syntax similar to unittest:

- A dot (.) means that the test passed.
- An F means that the test has failed.
- An E means that the test raised an unexpected exception.
---

* Fixtures for handling test dependencies, state, and reusable functionality
* Marks for categorizing tests and limiting access to external resources
* Parametrization for reducing duplicated code between tests
* Durations to identify your slowest tests
* Plugins for integrating with other frameworks and testing tools


# Testing The Code
The good news is, you’ve probably already created a test without realizing it. Remember when you ran your application and used it for the first time? Did you check the features and experiment using them? That’s known as exploratory testing and is a form of manual testing.

Exploratory testing is a form of testing that is done without a plan. In an exploratory test, you’re just exploring the application.

To have a complete set of manual tests, all you need to do is make a list of all the features your application has, the different types of input it can accept, and the expected results. Now, every time you make a change to your code, you need to go through every single item on that list and check it.

This is where automated testing comes in. Automated testing is the execution of your test plan (the parts of your application you want to test, the order in which you want to test them, and the expected responses) by a script instead of a human. Python already comes with a set of tools and libraries to help you create automated tests for your application. We’ll explore those tools and libraries in this tutorial.

---
## Unit test and Integration test.
A unit test is a smaller test, one that checks that a single component operates in the right way. A unit test helps you to isolate what is broken in your application and fix it faster.

An integration test checks that components in your application operate with each other.
A unit test checks a small component in your application.
You can write both integration tests and unit tests in Python.

---

# How to Structure a Simple Test

1. What do you want to test?
2. Are you writing a unit test or an integration test?

Then the structure of a test should loosely follow this workflow:

4. Create your inputs
5. Execute the code being tested, capturing the output
6. Compare the output with an expected result