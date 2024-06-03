# Qoherent's Coding Guidelines

To ensure smooth development, reduce frustration, and minimize conflicts, we kindly insist that all code 
contributions must adhere to these guidelines.

Think there's a better approach? We encourage challenges and discussions to continuously enhance and 
refine our approach. You're welcome to present your ideas and rationale on our [ideas forum](https://github.com/qoherent/ria/discussions/categories/ideas).


## 📝 General guidelines

Limit lines to 119 characters. This includes code, comments, docstrings.

All contributions must include appropriate tests.

All contributions must be well documented, with a copious amount of complete docstrings.

All contributions must adhere to the project's linting and formatting specifications.


## 🐍 Python-specific guidelines

Python project's should be typed. Please include complete type annotations for all function parameters and return 
values.

Adhere to the [PEP-8](https://peps.python.org/pep-0008/) guidelines.

Prefer [keyword arguments](https://docs.python.org/3/glossary.html#term-argument?highlight=keyword%20argument) over positional arguments.

We utilize [Black](https://black.readthedocs.io/en/stable/) for automated code formatting, with configuration settings often defined in `pyproject.toml`. 
Please ensure that all code contributions are auto-formatted with Black, this is important to ensure consistent and 
reliably formatted code.

We rely on [isort](https://pycqa.github.io/isort/index.html) for import sorting, with configuration settings often defined in `pyproject.toml`. Please use
isort to automatically organize your import statements.

We use [Flake8](https://flake8.pycqa.org/en/latest/) for code linting and style. All Python code must be formatted in accordance with the project's
Flake8 configuration settings defined in [tox.ini](../tox.ini).

We use [Sphinx](https://www.sphinx-doc.org/en/master/) to auto-generate the documentation for our Python projects. All docstrings must adhere to the 
[Sphinx docstring format](https://sphinx-rtd-tutorial.readthedocs.io/en/latest/docstrings.html#the-sphinx-docstring-format) and should include doctests 
showcasing clear and accessible examples of how to use the code.

Types mentioning in the docstring should be expressed in plain English rather than using Python's type hint syntax 
For example, write "int or float, optional" instead of "Optional[int | float]".

We prefer [pytest](https://docs.pytest.org/en/8.0.x/) to make our Python unit testing more efficient and expressive.

### Dependency management

Please use whichever environment manager is appropriate for the application. If you are working with more complicated 
software stacks or multiple programming languages, opt for [Conda](https://conda.io/projects/conda/en/latest/user-guide/getting-started.html).

To ensure a consistent development environment, we suggest [Poetry](https://python-poetry.org/) to resolve and lock dependencies. 
[Start here](https://python-poetry.org/docs/basic-usage/) for information on basic Poetry usage. Please refrain from making unnecessary updates to the
`poetry.lock` files.

### Command line interfaces

Prefer using [Click](https://click.palletsprojects.com/en/8.1.x/) to build your command-line interfaces (CLIs). Projects that are part of RIA must use Click, 
and should place commands is a separate `commands.py` file. By applying the `click.command` decorator, these commands
can be easily integrated with the rest of RIA.


## ⌨️ C-specific guidelines

**Coming soon:** We are still developing our C-specific coding guidelines and the corresponding continuous integration (CI) 
tests. In the meantime, please format your C code in accordance with [Google's C/C++ Style Guide](https://google.github.io/styleguide/cppguide.html).


## 🐙 Guidelines for Git and GitHub

Repository names should be normalized in alignment with PyPA: [Names and normalization](https://packaging.python.org/en/latest/specifications/name-normalization/).

Development should adhere to the standard [Git feature branch workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow).

Branch names should begin with the corresponding issue number. For instance, if you are addressing issue #7 
regarding README updates, your branch should be named as follows: "7-readme-updates".

Consider pushed work final unless you have a good reason to change it, and avoid making changes to the commit history 
of branches with open pull requests.

Please keep your commits [atomic](https://www.pauline-vos.nl/atomic-commits/). This makes your changes easier to understand and review.

Please keep your pull requests concise and focused. We recommend limiting your pull requests to around 300 lines.

We don’t have a commit template or any formal guidelines. Rather, we rely on each other to exercise good judgment and 
prioritize meaningful commit messages.


## 🙏 Thank you

A heartfelt thank you from everyone at Qoherent and the broader radio community for taking the time to review and 
adhere to these guidelines. These efforts significant enhance the efficiency and effectiveness of the development 
process, and make all our lives a little bit easier! 💖
