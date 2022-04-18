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


