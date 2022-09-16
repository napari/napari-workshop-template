# napari-workshop-template

A JupyterBook template for napari workshops.

**To see the built website, go to https://melissawm.github.io/napari-workshop-template**

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
jupyter book build napari-workshops
```

where `napari-workshops` is the name of the folder where your book is stored.
The rendered version of the workshop materials will be under
`napari-workshops/_build/html`. For more information, see the
[JupyterBook documentation](https://jupyterbook.org/).

**Note:** The html files built by the `jupyter book` commands do not need to be
stored on GitHub, so we added the following path to our `.gitignore` file:

```
napari-workshops/_build/
```

## Publish your workshop materials as a static web page

If you want to set up this material to be published as a website using [GitHub
pages](https://pages.github.com/), follow the steps below.

1. Edit the `.github/workflows/pages.yml` file in your workshop folder to
   include any installation or setup requirements. By default, the following
   commands are run as a setup and build step:

    ```
    - name: Build workshop
      run: |
        python -m pip install -r requirements.txt
        jupyter book build napari-workshops
    ```
2. Edit the `.github/workflows/pages.yml` file in your workshop folder to
   set up the desired folder there the (html) built artifacts are stored. By
   default, the artifacts are in the following path:

    ```
    - name: Upload artifact
      uses: actions/upload-pages-artifact@v1
      with:
        path: 'napari-workshops/_build/html'
    ```

As currently configured, whenever a new commit is added to the `main` branch of
this repository, a new deployment is made (the Jupyter book is built, and the
generated pages are uploaded). You can find the workshop materials at

```
https://<your-username>.github.io/<workshop-name>
```

For this template, the built site is at

https://melissawm.github.io/napari-workshop-template

## Publish your workshop materials as live notebooks

If you want to set up this material to be used as live notebooks, meaning folks
can edit and execute them using the [mybinder.org](https://mybinder.org/)
service, follow the steps below.

TODO

## Index your workshop using Zenodo (for citation purposes)

If you want people to be able to cite your workshop materials, you can create
a DOI for it using [Zenodo](https://zenodo.org/).

TODO

## Enable a citation file for your repository

Check [the GitHub documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files) for more details on how to use the `citation.cff` file to enable other to cite your repository.
