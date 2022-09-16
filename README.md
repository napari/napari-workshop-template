# napari-workshop-template

A JupyterBook template for napari workshops.

## Build locally

To build this workshop locally and preview your workshop materials, follow the
steps below.

1. Install all required packages

In a console/terminal, after installing python on your system using the
distribution of your choice, and ideally
[using a virtual environment](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/),
run

```
python -m pip install -r requirements.txt
```

2. Build your book

To render the html version of your book, including autogenerating figures or
running Jupyter notebooks, run

```
jupyter book build workshop
```

where `workshop` is the name of the folder where your book is stored. The
rendered version of the workshop materials will be under
`workshop/_build/html`. For more information, see the
[JupyterBook documentation](https://jupyterbook.org/).

## Publish your workshop materials as a web page

If you want to set up this material to be published as a website using [GitHub
pages](https://pages.github.com/), follow the steps below.

TODO

## Index your workshop using Zenodo (for citation purposes)

If you want people to be able to cite your workshop materials, you can create
a DOI for it using Zenodo.

TODO