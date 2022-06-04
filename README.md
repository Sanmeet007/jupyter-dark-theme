## Custom dark theme for Jupyter Notebooks

The best dark jupyter theme for your web browser. It's simple and coherent. It's one beautiful dark theme (dark skin) for your jupyter notebook. Protects your eyes from the white color in dark.

## Preview

<img width="1008" alt="Screenshot 2021-03-10 at 8 16 46 PM" src="https://sanmeet007.github.io/python-protos/images/Screenshot%20(60).png">

<img width="1008" alt="Screenshot 2021-03-10 at 8 16 18 PM" src="https://sanmeet007.github.io/python-protos/images/Screenshot%20(59).png">

<img width="1008" alt="Screenshot 2021-03-10 at 8 17 27 PM" src="https://sanmeet007.github.io/python-protos/images/Screenshot%20(56).png">

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

> Note : You will need to run that every time you start a notebook, and the matplotlib theme will not be applied. See below for a more permanent installation

---

For a permanent installation, we first need to copy `custom.css` file to `~/.jupyter/custom/custom.css`.

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
