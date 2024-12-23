# Jupyter book

This webpage is built using [Jupyter book](https://jupyterbook.org/en/stable/intro.html), which is a tool to generate webpages from `markdown`, `restructured text`,`python notebooks` and many other formats.

A Jupyter book can consist of a combination of these kinds of files, and can allow users to interact with the code and visualize the results.
Examples can be found at:
- [FEniCSx tutorial](https://jorgensd.github.io/dolfinx-tutorial/)
- [Simcardems](https://computationalphysiology.github.io/simcardems/)
- [Oasisx](https://computationalphysiology.github.io/oasisx/)
- [Cardiac Geometries](https://computationalphysiology.github.io/cardiac-geometries/)
- [Action Potential Features](https://computationalphysiology.github.io/ap_features/)
- [Cardiac MPS Motion](https://computationalphysiology.github.io/mps_motion/)

There are two files that are required to build a Jupyter book, the _Table of Contents_ and the _Configuration_-file.

A good guide for setting up the book can be found at: [Jupyterbook - Official documentation](https://jupyterbook.org/en/stable/start/create.html)

## Installation and building
Jupyter-book can be installed with `pip`
```bash
python -m pip install jupyter-book
```
and building the book can be done with the following command
```bash
jupyter-book build path/to/_config.yml
```

## `_toc.yml`
A `yaml` file listing the contents of the book. See: [Jupyterbook - Table of Contents](https://jupyterbook.org/en/stable/structure/toc.html) for more information.

## `_config.yml`
A configuration file for the book, see: [Jupyterbook - Configuration reference](https://jupyterbook.org/en/stable/customize/config.html) for the full list of options.

(publishing-book)=
## Publishing book
The book can be published following [Publishing to Pages](#publishing-to-pages), where
step 3 in the official action would be calling `jupyter book build .` to generate the documentation at `_build/html`, which in turn is the folder we upload as a Github page.

A Github action showing some of the steps can be found at [Actions/deploy-pages](https://github.com/actions/deploy-pages#usage).


## Automatic building of Package API

For packages, one can use the [auto-doc](https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html)-extension of Sphinx to automatically generate an API for the Python package.
See: [Jupyterbook - Package API](https://jupyterbook.org/en/stable/advanced/developers.html?highlight=api#developer-workflows) for more information.

An example of the automatically generated API can be found at <https://scientificcomputing.github.io/example-python-package/docs/api.html>
