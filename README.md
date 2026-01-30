# APS699_Sp2026
 Materials for APS699 - Spring 2026

## Python libraries
xarray, pandas, cartopy, arm_pyart, satpy, metpy, boto, cfgrib, sharppy, jupyterlab.

## Quick start
### JupyterLab login
Log in to your JupyterLab account at https://jupyter.cas.hamptonu.edu and open a terminal inside JupyterLab.

### Python and libraries check
Confirm your working directory:
```
pwd
echo $HOME
```
Move to your home directory (if you are not already there):
```
cd "$HOME"
pwd
```
Check Python and pip:
```
python --version
python -m pip --version
```
Verify one required library (example):
```
python -m pip show xarray
```
Verify the full list of required libraries:
```
python -m pip list | grep -E "^(xarray|pandas|cartopy|arm_pyart|satpy|metpy|boto|cfgrib|sharppy|jupyterlab)\\b"
```

### Create and activate Python environment
Create and activate the course conda environment:
```
conda env create -f APS699-Sp2026-HW1.yml
conda activate APS699-Sp2026-HW1
```
Launch JupyterLab from this environment (if needed):
```
jupyter lab
```

### Clone GitHub repository
Clone the course repository:
```
git clone https://github.com/mdfriberg/APS699-Sp2026.git
```
Move into the repo and list files:
```
cd APS699-Sp2026
ls
```

## Python environment setup
List available conda environments:
```
conda env list
```
Create a new conda environment file:
```
conda env create -f APS699-Sp2026-Test.yml
```
Add libraries to the environment by editing `APS699-Sp2026-Test.yml` and adding packages under `dependencies`. Recreate the environment after edits:
```
conda env remove -n APS699-Sp2026-Test
conda env create -f APS699-Sp2026-Test.yml
```
Activate the conda environment:
```
conda activate APS699-Sp2026-Test
```


