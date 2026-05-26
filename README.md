# How to run this notebook

You need **VS Code** with the **Python** and **Jupyter** extensions. If you don't have them yet, install them first:

1. [Download VS Code](https://code.visualstudio.com/)
2. Open VS Code, go to the Extensions tab (left sidebar), search for and install:
   - **Python** (by Microsoft)
   - **Jupyter** (by Microsoft)

## Quick start

1. Download this folder to your computer (if it's a `.zip`, unzip it first).
2. **Double-click** the setup script for your system:
   - **Mac**: `setup_mac.command`
   - **Windows**: `setup_windows.bat`
3. Wait. The first time it will download Python and the libraries (1-3 minutes).
4. When the script finishes, open this folder in VS Code:
   - **File → Open Folder...** and pick this folder.
5. Click on the notebook file (`.ipynb`) to open it.
6. VS Code will ask which Python interpreter to use. Choose the one inside this folder:
   - **Mac**: `.venv/bin/python`
   - **Windows**: `.venv\Scripts\python.exe`

After that, run cells with the play button on the left of each cell, or **Shift+Enter**.

You only need to run the setup script **once**. Next time, just open the folder in VS Code.

---

## First-time problems

### Mac: "cannot be opened because it is from an unidentified developer"

This is macOS's standard warning for downloaded scripts. Workaround:

1. **Right-click** (or Control-click) `setup_mac.command`
2. Choose **Open**
3. Click **Open** in the dialog

You only need to do this the first time.

### Mac: "permission denied"

Open Terminal (⌘+space → "Terminal"), drag `setup_mac.command` into the window, prefix the line with `chmod +x ` (mind the space), press Enter. Then close Terminal and double-click as normal.

### Windows: SmartScreen blocks the file

Click **More info** → **Run anyway**. This is normal for unsigned scripts.

### VS Code doesn't show the right interpreter

In the open notebook, click the interpreter selector in the top-right corner (it might say "Select Kernel"). Choose **Python Environments...** → the one with `.venv` in the path.

### Anything else

If `uv` install fails, you may be behind a corporate firewall. Ask IT to allow access to `astral.sh` and `pypi.org`.

---

## What does this actually install?

- **uv** — a small Python package manager, installed in your user folder (no admin rights needed)
- **Python 3.11** — downloaded into uv's cache, doesn't conflict with any Python you already have
- **Libraries** (matplotlib, prettytable, ipykernel) — installed inside `.venv/` in this folder, not system-wide

To uninstall: delete this folder. To remove uv as well: delete `~/.local/bin/uv` (Mac) or `%USERPROFILE%\.local\bin\uv.exe` (Windows).
