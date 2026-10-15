# JupyterLab tips screenshots

These PNGs accompany `../jupyterlab-basics.md`. They were captured from a running
local JupyterHub on 2026-10-15, rather than from the Pangeo@EOSC service.

- JupyterLab 4.6.4, light theme
- JupyterHub 5.5.3
- Jupyter Server 2.21.1
- Chrome on macOS (the menu shortcuts therefore use Command/Option)
- Browser viewport: 1100 × 740 CSS pixels, device scale factor 2
- A disposable `workshop` account, `practice.ipynb`, and `example-folder/notes.txt`

The images are direct browser screenshots, cropped to the relevant UI region.
They contain no production account or research data.

| Image | How to reproduce |
| --- | --- |
| `jupyterlab-run-menu.png` | Open a notebook, select a code cell below the first cell, then open **Run**. |
| `jupyterlab-kernel-menu.png` | With the notebook kernel running, open **Kernel**. |
| `jupyterlab-running-panel.png` | Start a notebook kernel and a terminal; open **Running Terminals and Kernels**. Widen the sidebar and collapse unrelated sections so both **Shut Down All** buttons are legible. |
| `jupyterlab-close-all-tabs.png` | Open **File** and hover over **Close All Tabs**. |
| `jupyterlab-hub-control-panel.png` | In a JupyterHub-managed Lab session, open **File**. |
| `jupyterhub-stop-server.png` | Choose **File > Hub Control Panel** while the user's server is running. |
| `jupyterlab-delete-folder.png` | In the file browser, right-click the disposable non-empty folder. |
| `jupyterlab-delete-nonempty-error.png` | Choose **Delete** and confirm, with the deletion settings below. |

For the non-empty-folder error, the disposable Jupyter Server used:

```python
c.FileContentsManager.delete_to_trash = False
c.FileContentsManager.always_delete_dir = False  # default
```

This reproduces the server's actual refusal to permanently delete a non-empty
directory. Servers with trash support and other deletion settings can behave
differently. Do not change a shared server's settings just to reproduce a screenshot.
