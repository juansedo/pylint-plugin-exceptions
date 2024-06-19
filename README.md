# Pylint Plugin Exceptions

[![PyPI - Version](https://img.shields.io/pypi/v/pylint-plugin-exceptions.svg)](https://pypi.org/project/pylint-plugin-exceptions)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/pylint-plugin-exceptions.svg)](https://pypi.org/project/pylint-plugin-exceptions)

## About

This project is a Pylint plugin that forces to describe every possible exception
on a function docstring.

Example of **incorrect** code:

```python
def func():
    raise ValueError("This is a test")
```
```bash

```

Example of **correct** code:

```python
def func():
    """Docstring description...
    
    Raises:
        ValueError: Description of the exception.
    """
    raise ValueError("This is a test")
```

## Motivation

Some years ago, [a discussion](https://github.com/python/typing/issues/71)
about exception checker in Python was started. The user
[Dakkaron](https://github.com/python/typing/issues/71#issuecomment-587351766)
proposed a solution using a *function inside a type checker* due to negative of
Guido Van Rossum about including
[any type of exception checking](https://github.com/python/typing/issues/71#issuecomment-87767297)
into the Python core.

**Table of Contents**

- [Installation](#installation)
- [License](#license)

## Installation

```console
pip install pylint-plugin-exceptions
```

## License

`pylint-plugin-exceptions` is distributed under the terms of the [MIT](https://spdx.org/licenses/MIT.html) license.
