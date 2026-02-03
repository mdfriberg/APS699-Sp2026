# APS699_Sp2026
 Materials for APS699 - Spring 2026

## Getting Started

### Conda vs pip (important)
- Use `conda` to install and manage packages for this course.
- Avoid mixing `pip` with `conda` in the same environment; it can override conda packages and cause dependency conflicts.
- If you must use `pip`, install conda packages first, then `pip`, and be ready to recreate the environment if conflicts appear.

### JupyterLab login
1. Log in to your JupyterLab account at https://jupyter.cas.hamptonu.edu.
2. Open a terminal inside JupyterLab.

### Python and libraries check
3. Confirm your working directory:
   - `pwd`
   - `echo $HOME`
4. Move to your home directory (if you are not already there):
   - `cd "$HOME"`
   - `pwd`
5. Check Python and conda:
   - `python --version`
   - `conda --version`
6. Show all installed libraries in conda:
   - `conda list`
7. Verify one required library (example):
   - `conda list xarray`
8. Verify the full list of required libraries:
   - `conda list | grep -E "^(xarray|pandas|cartopy|arm_pyart|satpy|metpy|boto|cfgrib|sharppy)\b"`

### Python environment setup
9. List available conda environments:
   - `conda env list`
10. Create a new conda environment file:
   - `conda env create -f APS699-Sp2026-Test.yml`
11. Add libraries to the environment by editing `APS699-Sp2026-Test.yml` and adding packages under `dependencies`. Recreate the environment after edits:
   - `conda env remove -n APS699-Sp2026-Test`
   - `conda env create -f APS699-Sp2026-Test.yml`
12. Activate the conda environment:
   - `conda activate APS699-Sp2026-Test`
13. Check for library conflicts (dry run):
   - `conda install --dry-run xarray pandas cartopy arm_pyart satpy metpy boto cfgrib sharppy jupyterlab`
14. Check environment health:
   - `conda info`
   - `conda list`
   - `conda install --dry-run xarray`
   - `python -c "import numpy, pandas; print('ok')"`
   - `conda list --explicit > /tmp/explicit.txt`

### Clone GitHub repository
15. Clone the course repository:
   - `git clone https://github.com/mdfriberg/APS699-Sp2026.git`
16. Move into the repo and list files:
   - `cd APS699-Sp2026`
   - `ls`
