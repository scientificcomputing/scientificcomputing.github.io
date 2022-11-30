# Create an installable package

In this section we will cover how to easily make an installable Python package.

## Repository structure
We recommend using the source layout. See [this chapter](https://py-pkgs.org/04-package-structure.html#the-source-layout) for justification. This means that from the root of your Github repository you should have a folder structure like
```
├── .git
├── README.md
├── LICENSE
├── pyproject.toml
└── src
    └── name_of_package
        ├── __init__.py
        └── functions.py
```
### `.git`
The .git folder is covered in [Version control](./version_control)


### `README.md`
This file should contain a description of your package. This could include installation instructions or simple use-cases. It is written in the [Markdown](https://www.markdownguide.org/).

### `LICENSE`
For other people to be able to use your software, it needs to have a license. For a list of available licenses see <https://spdx.org/licenses/>.

(content:pyproject)=
### `pyproject.toml`
A [toml](https://toml.io/en/) (Tom's Obivous Minimal Language) file is a plain-text file, consisting of [tables](https://toml.io/en/v1.0.0#table)
which are a selection of key-value pairs.

An example is
```toml
[project]
name = "catch_us"
authors = [
    {name = "Per Ulv", email = "per@acme.no"},
    {name = "Bippe Stankelbein", email = "bippe@roadrunner.no"}
    ]
version = "x.y.z"
requires-python = ">=3.8"

# Short description
description = "Meep Meep"

# Path to README.md
readme = "README.md"

# Path to license file
license = {file = "LICENSE"}

# Direct dependencies
dependencies = [
    'acme',
    'numpy'
]
```

#### Optional dependencies
The core functionality of a package (its classes and functions) might not depend on many other packages.

However, to be able to test the code, check for consistency and create coverage reports, one might meed additional dependencies.

One can therefore specify a second table in the `pyproject.toml` file, called
[project.optional-depencies].
This is treated as a sub-table of `project`.

For instance, if you want to test your package with [pytest](https://docs.pytest.org/en/7.1.x/), you can add
```toml
[project.optional-dependencies]
test = ["pytest"]
```
Then, when installing the package, you call `pip3 install .[test]` instead of `pip3 install .` to get the additional dependencies.

#### Other tables
For options related to coverage reports and code consistency, see the [Coverage](./python-coverage) and [Linting](./python-linting.md) section, respectively.
