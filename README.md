![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)

# scientificcomputing.github.io

The resources for generating <https://scientificcomputing.github.io/>.

## How to add a paper with repository?

Please fill in [https://github.com/scientificcomputing/scientificcomputing.github.io/issues/new?assignees=&labels=new-repo&projects=&template=repository.yml&title=%5BAdd+repo%5D%3A+](https://github.com/scientificcomputing/scientificcomputing.github.io/issues/new?assignees=&labels=new-repo&projects=&template=repository.yml&title=%5BAdd+repo%5D%3A+)

## How to add a paper relating to a software?

Please fill in [https://github.com/scientificcomputing/scientificcomputing.github.io/issues/new?assignees=&labels=new-package&projects=&template=package.yml&title=%5BAdd+package%5D%3A+](https://github.com/scientificcomputing/scientificcomputing.github.io/issues/new?assignees=&labels=new-package&projects=&template=package.yml&title=%5BAdd+package%5D%3A+)

# Contribute to the webpage

To contribute, please make a fork of the repository and clone it to your local system, then make a new branch with

```bash
git checkout -b name_of_author/describe_feature
```

Then add the relevant text.
Next ensure that the webpage builds, this can be done with

```bash
python3 -m venv sc_webpage_env
source sc_webpage_env/bin/activate
python3 -m pip install .
python3 -m jupyter book build -W ./docs
```

Inspect the webpage locally by opening `./docs/_build/html/index.html` and navigating to the appropriate page.

Before you push the changes, ensure that the text is properly formatted, run

```bash
pre-commit
```

Then, make corrections and commit any changes before re-running pre-commit.

Push the branch to your fork, and then make a pull request through the github web-interface.
