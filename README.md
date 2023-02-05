## Custom dark theme for Jupyter Notebooks


The best dark jupyter theme for your web browser. It's simple and coherent. It's one beautiful dark theme (dark skin) for your jupyter notebook. Protects your eyes from the white color in dark.

## Preview

<img width="1008" alt="Jupyter Notebook" src="https://i.ibb.co/LNh5g2c/Screenshot-203.png">
<img width="1008" alt="Jupyter Notebook" src="https://i.ibb.co/93qDd2X/Screenshot-204.png">

## Requirements

- Python 3.10 or higher
- Jupyter
- Chrome browser ( recommended v100.0 or above )

## Installation

#### Custom CSS Theme

You can directly invoke the CSS inside a notebook like this:

```python
from IPython.core.display import HTML, display
from urllib.request import urlopen

CSS_URL = "https://raw.githubusercontent.com/Sanmeet007/jupyter-dark-theme/main/dist/custom.css"
CSS = urlopen(CSS_URL)
CSS = CSS.read().decode('utf-8')
HTML_CSS = f"""
<style>
{CSS}
</style>
"""
HTML(HTML_CSS)
```

> Note : You will need to run that every time you start a notebook. See below for a more permanent installation

---

For a permanent installation, we first need to copy `custom.css` file to `~/.jupyter/custom/custom.css`.

#### Using windows cmd and explorer

First we need to generate the config for the jupyter notebook.After this we need to paste our `custom.css` file to `~/.jupyter/custom/`.

```bash
jupyter notebook --generate-config
cd .jupyter
mkdir custom # may already exist
explorer .
```

Now paste the downloaded `custom.css` file here in this file location `~/.jupyter/custom/`

#### Checking if css was installed correctly

```
jupyter notebook
```

> Note : Here the `~` denotes the path before the .jpuyter folder.

#### Using bash only

```bash
cd ~/.jupyter
mkdir custom  # may already exist
cd .jupyter/custom
rm custom.css
wget https://raw.githubusercontent.com/Sanmeet007/jupyter-dark-theme/main/dist/custom.css
```

## Printing

As recommended use the lastest chrome browser . For printing use the `Ctrl + P` command .

> Note : The print preview doesn't shows the exact printing because of custom css applied

## Inspiration / Sources

This repo is deeply inspired by:

- [JupyterThemes by Dunovank](https://github.com/dunovank/jupyter-themes)
- [Custom Ocean-y Dark Theme for Jupyter Notebooks by Rahul Somani](https://github.com/rsomani95/jupyter-custom-theme)
