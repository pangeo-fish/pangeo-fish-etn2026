# Practical tips for JupyterLab

If you are not yet familiar with JupyterHub, JupyterLab or the Python environment,
this page gathers a few practical tips that are useful during (and after) the workshop.

## Run the cells of a notebook

- Run **one cell**: click in it and press `Shift + Enter` (or the ▶ button in the toolbar).
- Run **all cells** from the top: `Run > Run All Cells`.
- Start again from a clean state: `Kernel > Restart Kernel and Run All Cells…`.
- Run everything up to where you are: `Run > Run All Above Selected Cell`.

While a cell runs, it shows `[*]` on its left and the kernel status (top right) is a
filled circle ●. When it is finished, `[*]` becomes a number such as `[12]`.

To stop a cell that takes too long: ■ button in the toolbar, or `Kernel > Interrupt Kernel`.

## Save your work

`File > Save Notebook` (`Ctrl + S`, or `Cmd + S` on a Mac). Your home directory on
Pangeo@EOSC is persistent: files you save are still there the next time you log in.

## Shut down kernels and close tabs

Closing a notebook tab does **not** stop its kernel: it keeps running and keeps its
memory. When you are done with a notebook:

- `Kernel > Shut Down Kernel` for the current notebook, or
- `Kernel > Shut Down All Kernels…` for all of them, or
- the **Running Terminals and Kernels** panel in the left sidebar (■ in a circle icon):
  click `Shut Down All` next to "Kernels" and "Terminals".

Then close all tabs with `File > Close All Tabs`.

## Stop your server when you are done

Your JupyterLab server keeps using CPU, memory and electricity on the shared
infrastructure until it is stopped, even when you close the browser. Please stop it
at the end of the session:

1. `File > Hub Control Panel`
2. click **Stop My Server**
3. (optional) `File > Log Out`

Stopping the server does not delete your files. Next time, click **Start My Server**
(or the one-click workshop link) to start it again.

## Delete a folder

In the file browser (left sidebar), right-click a file or folder and choose `Delete`.
A folder that still contains files cannot be deleted this way. Two options:

- **File browser**: open the folder, select all files (`Shift + click` the first and
  last), right-click > `Delete`, go back up and delete the now empty folder.
  Hidden files (names starting with `.`, such as `.ipynb_checkpoints`) are not shown and
  can still block the deletion; use the terminal in that case.
- **Terminal** (`File > New > Terminal`):

  ```bash
  cd ~
  ls                      # check the exact folder name
  rm -rf name-of-the-folder
  ```

  :::{warning}
  `rm -rf` deletes the folder and everything inside it immediately and permanently.
  There is no trash. Check the name twice.
  :::

To clean up the workshop entirely, delete the `pangeo-fish-etn2026` folder in your
home directory; the one-click link clones it again if you need it.

## Upload and download files

- **Upload**: drag files from your computer onto the file browser, or use the ⬆ button.
- **Download**: right-click a file in the file browser > `Download`.
  (For a folder, compress it first in a terminal: `zip -r results.zip my-folder`.)
