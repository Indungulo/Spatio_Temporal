# Spatio_Temporal
Spatial Analysis of Mapped 3D Timeseries Data

## Project Overview

This repository contains simple, step-by-step code to perform spatio-temporal analyses of sea surface temperature (SST) using daily CMEMS OSTIA L4 data. It covers:
1. Loading netCDF SST data
2. Extracting values from one pixel, a box, or the full scene.
3. Testing for long-term trends (Mann–Kendall).
4. Visual and Statistical comparison of subregions.

> **Note:** This is not a sophisticated production pipeline — it’s designed for those just learning to work with CMEMS netCDF files in Python.

---

## Data Source

In this notebook, I use the **OSTIA Global Sea Surface Temperature & Sea Ice Analysis** (L4, 0.05° × 0.05° daily) from CMEMS:

* Data are free but access requires registration at [CMEMS Data Portal](https://marine.copernicus.eu/)
* **Product DOI:** [https://doi.org/10.48670/moi-00168](https://doi.org/10.48670/moi-00168)
* Foundation SST: gap-free maps of SST (no diurnal variability) and ice concentration (Good et al., 2020)

---

## Usage

1. **Download** your CMEMS SST `.nc` file (e.g., `sst.nc`).
2. **Open** the notebook `CMEMS_Spatio-Temporal.ipynb`.
3. **Edit** file path and any geographic subset parameters.
4. **Run** all cells in order:

   * Data import & pre-processing
   * Trend testing (Mann–Kendall)
   * Rolling mean/std and anomaly detection
   * Statistical tests (Kruskal–Wallis, Dunn’s post-hoc)
   * Pixel-wise slope map with Cartopy

---

## Reference

> Good, S.; Fiedler, E.; Mao, C.; Martin, M.J.; Maycock, A.; Reid, R.; Roberts-Jones, J.; Searle, T.; Waters, J.; While, J.; Worsfold, M.
> *The Current Configuration of the OSTIA System for Operational Production of Foundation Sea Surface Temperature and Ice Concentration Analyses.*
> Remote Sens. 2020, 12, 720. doi:10.3390/rs12040720

---

## License

Distributed under the MIT License. See `LICENSE` for details.
