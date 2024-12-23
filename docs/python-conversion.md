# Conversion to and from Jupyter notebooks

## Python -> Notebook
One can use [jupytext](https://jupytext.readthedocs.io)

```bash
jupytext --to=ipynb --output=path_to_nb.ipynb
```

The Python file should follow the conventions of the [light format](https://jupytext.readthedocs.io/en/latest/formats-scripts.html#the-light-format) for appropriate rendering.

## Notebook -> Python
You can add meta-data to your notebook, making it auto convert to a Python-file at saving (using JupyterLab). This can be achieved by pressing `ctrl+shift+c` and choose `Pair notebook with light script`.

You could also directly modify the notebook metadata with:
```yaml
{
# Other options
#....
"jupytext": {
    "formats": "ipynb,py:light"
}
}
```

One can also use [pre-commit](https://pre-commit.com/) hooks to automatically sync notebooks with a corresponding file, see [here](https://jupytext.readthedocs.io/en/latest/using-pre-commit.html)
