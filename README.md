# Documentation for TeSS Platform

Separate the training docs/help content to separate repo, like [IBISBA Handboook](https://ibisba.github.io/workshop/docs/intro.html).

Built using [Jupyter Book 1](https://jupyterbook.org/). For additional guidance, see:

- [Anatomy of a Jupyter Book (TeachBooks.io)](https://teachbooks.io/manual/basic-features/jupyterbook.html)
- [Sphinx Design (the engine behind Jupyter Book)](https://sphinx-design.readthedocs.io/en/latest/) including [CSS classes](https://sphinx-design.readthedocs.io/en/pydata-theme/css_classes.html)
- [MyST Syntax Extensions](https://myst-parser.readthedocs.io/en/latest/syntax/optional.html) even though we are using Markdown, not MyST

To run locally, install Jupyter Book then build:
```shell
pip install -U jupyter-book
jupyter-book build TeSS_docs/
```