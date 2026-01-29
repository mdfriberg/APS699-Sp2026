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
1. Clone the GitHub project:
   - `git clone https://github.com/mdfriberg/APS699-Sp2026.git`
2. Print the Python version:
   - `python --version`
3. Print the list of libraries:
   - `python -m pip list`
4. Check if required libraries are installed:
   - `python -m pip list | grep -E "^(xarray|pandas|cartopy|arm_pyart|satpy|metpy|boto|cfgrib|sharppy|jupyterlab)\b"`


## Python environment setup
Use the provided conda environment file:
- `conda env create -f APS699-Sp2026-HW1.yml`
- `conda activate APS699-Sp2026-HW1`

## Data summary tables
These tables summarize datasets used in the course and separate sources into raw observational data, model or reanalysis outputs, and value-added derived products. The separation highlights what is directly measured versus what is simulated and what is computed or curated from upstream sources.

### Observational datasets
| Dataset / Campaign | Data Type | Platform / Instrument | Temporal Coverage | Spatial Coverage | Access URL | Data Policy |
|-------------------|-----------|-----------------------|-------------------|------------------|------------|-------------|
| NOAA Tail Doppler Radar (TDR) | Doppler wind fields | NOAA aircraft-mounted radar | Campaign-specific | Hurricane inner-core & BL | https://www.aoml.noaa.gov/hrd/data_sub/ | NOAA Open Data |
| IWRAP | Vertical wind & precipitation | Airborne radar profiler | Campaign-specific | Hurricanes | https://www.aoml.noaa.gov/hrd/technology/iwrap/ | NOAA Open Data |
| ACTIVATE | Aerosol, cloud, meteorology | Aircraft + in situ | 2019–2022 | W. North Atlantic | https://espo.nasa.gov/activate | NASA Open Data |
| HSRL-2 | Aerosol lidar backscatter | Airborne lidar | 2019–2022 | W. North Atlantic | https://www.esrl.noaa.gov/csl/groups/csd/projects/hsrl/ | NASA/NOAA |
| RSP | Aerosol optical properties | Airborne polarimeter | 2019–2022 | W. North Atlantic | https://airbornescience.nasa.gov/instrument/RSP | NASA Open Data |
| CUPiDS | Urban plume winds | Airborne Doppler lidar | 2023 | Coastal urban | https://www.esrl.noaa.gov/csl/ | NOAA Open Data |
| USOS | Ozone & BL dynamics | Airborne Doppler lidar | 2024 | Utah | https://www.esrl.noaa.gov/csl/ | NOAA Open Data |
| AMMBEC | Methane plume winds | PUMAS mobile lidar | 2024 | Colorado | https://www.esrl.noaa.gov/csl/ | NOAA Open Data |
| Lufft CHM15k Ceilometer | Aerosol backscatter | Ground-based lidar | 2022–2024 | Hampton Univ., VA | https://www.lufft.com | Open Use |
| NASA AERONET | AOD, size distribution | CIMEL Sun photometer | 2017–present | Global | https://aeronet.gsfc.nasa.gov | NASA Open Data |
| CALIPSO / CALIOP | Spaceborne aerosol lidar | Satellite | 2006–present | Global | https://asdc.larc.nasa.gov/project/CALIPSO | NASA EOSDIS |
| Radiosondes | T, RH, wind profiles | Balloon soundings | Case-based | Regional | https://www.ncei.noaa.gov/products/weather-balloon | NOAA Open Data |
| WFIP-3 | Offshore wind obs | Multi-instrument campaign | 2024–present | Coastal New England | https://psl.noaa.gov/wfip3/ | NOAA / DOE |
| 915 MHz Radar Wind Profilers | Wind profiles | Ground-based radar | 2023–2025 | Block Island, Nantucket | https://psl.noaa.gov/data/obs/ | NOAA Open Data |
| Doppler Wind Lidars (WFIP-3) | Wind profiles | Ground-based lidar | 2024–present | WFIP-3 sites | https://psl.noaa.gov | NOAA Open Data |
| Infrared Spectrometers (ASSIST-II) | Thermodynamic profiles | Ground-based IR | 2024–present | WFIP-3 sites | https://psl.noaa.gov/data/obs/ | NOAA Open Data |
| Microwave Radiometers (MP-3000) | T, RH profiles | Ground-based radiometer | 2024–present | WFIP-3 sites | https://psl.noaa.gov/data/obs/ | NOAA Open Data |
| Ceilometers (WFIP-3) | Cloud base, fog | Ground-based lidar | 2024–present | WFIP-3 sites | https://psl.noaa.gov/data/obs/ | NOAA Open Data |
| DOE WindSentinel Buoy | Offshore wind profiles | Doppler lidar buoy | 2014–2016 | Offshore Virginia | https://a2e.energy.gov/projects/windsentinel | DOE Open Data |

### Model or reanalysis datasets
| Model / Dataset | Model Type | Resolution | Temporal Coverage | Domain | Access URL | Data Policy |
|-----------------|------------|------------|-------------------|--------|------------|-------------|
| WRF | Mesoscale NWP | Configurable | Case-based | Regional | https://www2.mmm.ucar.edu/wrf/users/ | NCAR / NSF |
| Fast-J / Fast-JX | Photolysis RT model | Column-based | Case-based | Vertical columns | https://github.com/NCAR/Fast-JX | Open Source |
| HRRR v4 | Operational NWP | 3 km | 2023–2025 | CONUS | https://rapidrefresh.noaa.gov/hrrr/ | NOAA Open Data |
| RAP v5 | Mesoscale NWP | 13 km | Ongoing | CONUS | https://rapidrefresh.noaa.gov/rap/ | NOAA Open Data |
| PolCube (planned) | Satellite aerosol retrievals | N/A | Post-2026 | Global ocean | https://www.nasa.gov/smallsats | NASA Open Data |

### Derived datasets
| Derived Product | Source Data | Methodology | Purpose | Archive Plan |
|-----------------|-------------|-------------|---------|--------------|
| LLJ Event Catalogs | Radar, lidar, HRRR | Threshold-based detection (Whiteman/Vanderwende) | Offshore LLJ climatology | NOAA PSL / Zenodo |
| Temperature Advection | HRRR + observations | Line-integral method | Diagnose WAA/CAA | NOAA-compliant repo |
| Hub-height Wind Statistics | WindSentinel, WFIP-3 | Temporal & directional analysis | Offshore wind forecasting | DOE Open Data |
| Aerosol Layer Heights | HSRL-2, RSP | Backscatter gradient methods | Photolysis sensitivity | NASA EOSDIS |
| Photolysis Rate Sensitivity | Fast-J + ACTIVATE | Radiative transfer modeling | Air-quality impacts | NCAR repo |
| PBL Height Retrievals | Doppler lidar, PUMAS | Haar wavelet + variance | Boundary-layer structure | NOAA CSL |
| Aerosol Extinction Profiles | Ceilometer + AERONET | Overlap-corrected inversion | Air quality characterization | NASA/NOAA |
| 3-D Ice Shell Fields | Convection simulations | Thermo-mechanical modeling | Ocean-world interiors | Zenodo / NSF |

