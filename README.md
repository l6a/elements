# The Elements of Reproducible Science

A [Jupyter Book](https://jupyterbook.org/) for different abstractions
needed for reproducible science.

## Contributing

All materials in this Jupyter Book are stored a special flavour of
Markdown called
[MyST (or Markedly Structured Text)](https://myst-parser.readthedocs.io/).

To edit the materials locally as Jupyter Notebooks, simply use
Jupytext to create a pair notebook:
```
jupytext-3.10 --sync --to ipynb [chapter].md
```
All changed made to the notebook will be automatically synced to the
MyST markdown file.
