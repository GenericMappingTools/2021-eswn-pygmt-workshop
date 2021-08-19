---
title: ESWN 2021 - Writing unit tests
description: Tutorial for 2021 ESWN PyGMT workshop
slideOptions:
  theme: solarized
---

## Writing unit tests

*Because tested code is code that you can trust*

<!-- Put the link to this slide here so people can follow -->
<small> P.S. Slides are at https://hackmd.io/@pygmt/eswn-2021-writing-unit-tests</small>

---

## Why test?

Imagine choosing two vaccines :syringe::

- Vaccine 1 comes with the exact biochemical equations on how it works
- How vaccine 2 works is a mystery, but it has been extensively tested on thousands of people, across diverse populations, with little side effects

Which one would you choose :thinking_face:?

---

## Testing code helps to

- Ensure functions work as expected :green_heart: (even if they seem like a black box)
- Prevent bugs :bug: from popping up over time
- Give us confidence when refactoring :recycle: (i.e. rewriting) code to be more efficient, while keeping the same functionality

---

## Structure of a unit test 🧪

Let's start with a simple Python function that adds two numbers:

```python
def add(x, y):
    return x + y
```

Now let's check that this function works on two input numbers. We'll use a testing framework/library called [`pytest`](https://docs.pytest.org/en/6.2.x/) that allows us to easily check the output using `assert` statements.

```python
def test_add():
    value = add(x=1.0, y=2.0)
    assert value == 3.0
```

---

## Where do the tests go?

In a Python project using [`pytest`](https://docs.pytest.org/en/6.2.x/), we usually structure our code in folders like so:

```markdown
projectname/
  ├──src/
  │   └──calc.py (contains 'add' function)
  └──tests/
      └──test_calc.py (contains 'test_add' function)
```

The 'test_calc.py' file would contain:

```python
from projectname.src.calc import add

def test_add():
    value = add(x=1.0, y=2.0)
    assert value == 3.0
```

---

## Run tests using [`pytest`](https://docs.pytest.org/en/6.2.x/)

By default, `pytest` automatically searches for `test_*.py` files in the `tests` folder, and runs functions that start with a `test_`.

```bash
cd projectname/  # navigate to project folder
pytest           # run tests in tests/test_*.py files
```

will produce an output like so:

```python-traceback
==================== test session starts =====================
platform linux -- Python 3.8.10, pytest-6.2.4
rootdir: /home/user/projectname
collected 1 item

tests/test_calc.py .                         [100%]

===================== 1 passed in 0.03s ======================
```

---

## Run only specific tests 🎯

Projects can have >100 tests which take a long time to run. You can also run just one test file instead:

```bash
pytest projectname/tests/test_calc.py
```

Maybe that file has other functions like add/subtract/multiply/divide. You can be even more specific and run just the one that matches a keyword:

```bash
pytest -k add projectname/tests/test_calc.py
```

That's the basics of using [`pytest`](https://docs.pytest.org/en/6.2.x/) in a nutshell!

---

## Useful resources :open_book:

PyGMT's testing guidelines

<small>

- https://www.pygmt.org/v0.4.1/contributing.html#testing-your-code

</small>

Basics of testing in Python

<small>

- https://automationpanda.com/2017/03/14/python-testing-101-pytest
- https://realpython.com/python-testing and https://realpython.com/pytest-python-testing/

</small>

Test driven development

<small>

- https://realpython.com/courses/test-driven-development-pytest/
- https://dev.to/cheukting_ho/python-zero-to-hero-ep-13-test-driven-development-1g9l

</small>

---

### Thank you! :sheep:
