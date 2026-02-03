# APS699_Sp2026
 Materials for APS699 - Spring 2026

## Getting Started

### Conda vs pip (important)
- Use `conda` to install and manage packages for this course.
- Avoid mixing `pip` with `conda` in the same environment; it can override conda packages and cause dependency conflicts.
- If you must use `pip`, install conda packages first, then `pip`, and be ready to recreate the environment if conflicts appear.

### Clone GitHub repository
1. Clone the course repository:
   - `git clone https://github.com/mdfriberg/APS699-Sp2026.git`
2. Move into the repo and list files:
   - `cd APS699-Sp2026`
   - `ls`
3. Update an existing clone (if you already have one):
   - `git pull`

### JupyterLab login
4. Log in to your JupyterLab account at https://jupyter.cas.hamptonu.edu.
5. Open a terminal inside JupyterLab.

### Python and libraries check
6. Confirm your working directory:
   - `pwd`
   - `echo $HOME`
7. Move to your home directory (if you are not already there):
   - `cd "$HOME"`
   - `pwd`
8. Check Python and conda:
   - `python --version`
   - `conda --version`
9. Show all installed libraries in conda:
   - `conda list`
10. Verify one required library (example):
   - `conda list xarray`
11. Verify the full list of required libraries:
   - `conda list | grep -E "^(xarray|pandas|cartopy|arm_pyart|satpy|metpy|boto|cfgrib|sharppy)\b"`
12. Check for library conflicts (dry run):
   - `conda install --dry-run xarray pandas cartopy arm_pyart satpy metpy boto cfgrib sharppy jupyterlab`

### Python environment setup
13. List available conda environments:
   - `conda env list`
14. Create a new conda environment file:
   - `conda env create -f APS699-Sp2026-Test.yml`
15. To make your own environment, copy the yml file, edit the renamed yml file, then create and activate the new environment:
   - `cp APS699-Sp2026-Test.yml APS699-Sp2026-MyEnv.yml`
   - `vi APS699-Sp2026-MyEnv.yml`
   - `conda env create -f APS699-Sp2026-MyEnv.yml`
   - `conda activate APS699-Sp2026-MyEnv`
16. Check environment health:
   - `conda info`
   - `conda list`
   - `conda install --dry-run xarray`
   - `python -c "import numpy, pandas; print('ok')"`
   - `conda list --explicit > /tmp/explicit.txt`

### Reference links
- Python: https://www.python.org
- Conda: https://docs.conda.io
- Vi editor: https://www.vim.org
- JupyterHub: https://jupyter.cas.hamptonu.edu