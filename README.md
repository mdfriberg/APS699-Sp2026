# APS699_Sp2026
 Materials for APS699 - Spring 2026

## Python libraries
- xarray
- pandas
- cartopy
- arm_pyart
- satpy
- metpy
- boto
- cfgrib
- sharppy
- jupyterlab

## Quick start
### JupyterLab login
1. Log in to your JupyterLab account at https://jupyter.cas.hamptonu.edu.
2. Open a terminal inside JupyterLab.

### Python and libraries check
3. Confirm your working directory:
   - `pwd`
   - `echo $HOME`
4. Move to your home directory (if you are not already there):
   - `cd $HOME`
   - `pwd`
5. Check Python and pip:
   - `python --version`
   - `python -m pip --version`
6. Verify one required library (example):
   - `python -m pip show xarray`
7. Verify the full list of required libraries:
   - `python -m pip list | grep -E "^(xarray|pandas|cartopy|arm_pyart|satpy|metpy|boto|cfgrib|sharppy|jupyterlab)\b"`

### Create and activate Python environment
8. Create and activate the course conda environment:
   - `conda env create -f APS699-Sp2026-HW1.yml`
   - `conda activate APS699-Sp2026-HW1`
9. Launch JupyterLab from this environment (if needed):
   - `jupyter lab`

### Clone GitHub repository
10. Clone the course repository:
   - `git clone https://github.com/mdfriberg/APS699-Sp2026.git`
11. Move into the repo and list files:
   - `cd APS699-Sp2026`
   - `ls`

## Python environment setup
1. List available conda environments:
   - `conda env list`
2. Create a new conda environment file:
   - `conda env create -f APS699-Sp2026-Test.yml`
3. Add libraries to the environment:
   - Edit `APS699-Sp2026-Test.yml` and add packages under `dependencies`.
   - Recreate the environment after edits:
     - `conda env remove -n APS699-Sp2026-Test`
     - `conda env create -f APS699-Sp2026-Test.yml`
4. Activate the conda environment:
   - `conda activate APS699-Sp2026-Test`


