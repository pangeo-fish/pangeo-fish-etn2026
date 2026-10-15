# Practical tips for JupyterLab

If you are not yet familiar with JupyterHub, JupyterLab or the Python environment,
this page gathers a few practical tips that are useful during (and after) the workshop.

The screenshots below show a standard JupyterLab 4 session on JupyterHub, using a
small practice notebook. Your server may have slightly different menus or styling.
Keyboard shortcuts shown in the screenshots are for macOS.

## Run the cells of a notebook

- Run **one cell**: click in it and press `Shift + Enter` (or the ▶ button in the toolbar).
- Run **all cells** from the top: `Run > Run All Cells`.
- Start again from a clean state: `Kernel > Restart Kernel and Run All Cells…`.
- Run everything up to where you are: `Run > Run All Above Selected Cell`.

:::{figure} images/jupyterlab-run-menu.png
:alt: JupyterLab Run menu with Run All Above Selected Cell and Run All Cells.
:width: 800px

Use the **Run** menu to execute all cells or just the cells above the selected one.
:::

While a cell runs, it shows `[*]` on its left and the kernel status (top right) is a
filled circle ●. When it is finished, `[*]` becomes a number such as `[12]`.

To stop a cell that takes too long: ■ button in the toolbar, or `Kernel > Interrupt Kernel`.

:::{figure} images/jupyterlab-kernel-menu.png
:alt: JupyterLab Kernel menu with Interrupt Kernel, Restart Kernel and Run All Cells, and Shut Down All Kernels.
:width: 800px

The **Kernel** menu contains the interrupt, restart and shutdown commands.
:::

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

:::{figure} images/jupyterlab-running-panel.png
:alt: Running Terminals and Kernels sidebar with separate Shut Down All buttons for Kernels and Terminals.
:width: 440px

Open the running sessions panel using the circle-with-a-square icon on the left.
**Kernels** and **Terminals** each have their own **Shut Down All** button.
:::

Then close all tabs with `File > Close All Tabs`.

:::{figure} images/jupyterlab-close-all-tabs.png
:alt: JupyterLab File menu with Close All Tabs highlighted.
:width: 600px

After shutting down the kernels and terminals, choose **File > Close All Tabs**.
:::

## Stop your server when you are done

Your JupyterLab server keeps using CPU, memory and electricity on the shared
infrastructure until it is stopped, even when you close the browser. Please stop it
at the end of the session:

1. `File > Hub Control Panel`
2. click **Stop My Server**
3. (optional) `File > Log Out`

:::{figure} images/jupyterlab-hub-control-panel.png
:alt: JupyterLab File menu with Hub Control Panel near the bottom.
:width: 600px

First open **File > Hub Control Panel**.
:::

:::{figure} images/jupyterhub-stop-server.png
:alt: JupyterHub home page showing the red Stop My Server button beside My Server.
:width: 800px

Then click **Stop My Server** on the JupyterHub page.
:::

Stopping the server does not delete your files. Next time, click **Start My Server**
(or the one-click workshop link) to start it again.

## Delete a folder

In the file browser (left sidebar), right-click a file or folder and choose `Delete`.

:::{figure} images/jupyterlab-delete-folder.png
:alt: File browser context menu opened on example-folder, with the Delete command.
:width: 800px

Right-click the folder and choose **Delete**.
:::

Depending on the server's trash and deletion settings, a folder that still contains
files may be rejected with a **Directory ... not empty** error. Other servers can
move the entire folder to the trash.

:::{figure} images/jupyterlab-delete-nonempty-error.png
:alt: Delete Failed dialog reporting that example-folder is not empty.
:width: 700px

This server refuses to delete a non-empty folder. The path in your error will differ.
:::

If you get this error, there are two options. For folders with nested subfolders
(such as Zarr stores) or hidden files (names starting with `.`), using the terminal
is usually quicker than emptying each folder in the file browser.

- **File browser**: open the folder, select all files (`Shift + click` the first and
  last), right-click > `Delete`, go back up and delete the now empty folder.
  If there are subfolders, empty and delete them first. Hidden files are not shown
  by default and can still block deletion.
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
