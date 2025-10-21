# Documentation for TeSS Platform

https://elixirtess.github.io/docs/

Separate the training docs/help content to separate repo, like [IBISBA Handboook](https://ibisba.github.io/workshop/docs/intro.html).

Built using [Jupyter Book 1](https://jupyterbook.org/). For additional guidance, see:

- [Anatomy of a Jupyter Book (TeachBooks.io)](https://teachbooks.io/manual/basic-features/jupyterbook.html)
- [Sphinx Design (the engine behind Jupyter Book)](https://sphinx-design.readthedocs.io/en/latest/) including [CSS classes](https://sphinx-design.readthedocs.io/en/pydata-theme/css_classes.html)
- [MyST Syntax Extensions](https://myst-parser.readthedocs.io/en/latest/syntax/optional.html) even though we are using Markdown, not MyST

## Running locally and on GitHub Pages

Requirements:

- Python

To run locally, install Jupyter Book in a virtual environment then build:

```shell
python -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
pip install -U jupyter-book
jupyter-book build TeSS_docs/
```

And when you have finished, to quit virtual environment:

```shell
deactivate
```

We are hosting on GitHub Pages (using [Actions](https://github.com/ElixirTeSS/docs/blob/main/.github/workflows/main.yml)), using a different build command that means the `.html` part of the paths are not included. For example, we have page URLs like https://elixirtess.github.io/docs/accounts/user/ instead of ~~https://elixirtess.github.io/docs/accounts/user.html~~ -- this is achieved by rendering each page as a directory with its own `index.html` page. When running locally, this doesn't work so well, so use the default build command shown above.

The build command in the GitHub Action includes:

```shell
jupyter-book build --builder dirhtml TeSS_docs/
```
