
---
layout: home
---

# High-Performance Computing & Climate Data Analytics Showcase

Technical summary focused on multi-terabyte data architecture, computational physics, and advanced climate engineering simulations within the [**Community Earth System Model**](https://www.cesm.ucar.edu/models) (CESM GCM) framework.

### 🔬 Project Overview
This repository serves as a technical showcase of my research at **Cornell University**, focusing on large-scale data architecture and numerical modifications within the **CESM GCM** framework. The core objective is to simulate the spectral and bolometric impacts of space-based solar radiation management (SRM) strategies.

> 🖥️ **HPC Infrastructure:** All simulations and data pipelines were architected and executed on the [**NCAR Derecho**](https://www.cisl.ucar.edu/capabilities/derecho) High-Performance Computing (HPC) cluster, utilizing [**NetCDF4**](https://docs.unidata.ucar.edu/netcdf-c/current/) standards for high-throughput I/O of **60 TB+** datasets.

### 🤝 Research Collaborations
* **[National Center for Atmospheric Research](https://ncar.ucar.edu) (NCAR) in Boulder, CO:** Prof. Simone Tilmes.
* **[Planetary Sunshade Institute](https://planetarysunshade.org) (PSI) in Los Angeles, CA:** Morgan Goodwin.
* **[Department of Mechanical, Materials and Manufacturing Engineering (University of Nottingham, UK)](https://www.nottingham.ac.uk/engineering/departments/m3/index.aspx):** Prof. Chantal Cappelletti, Prof. Nishanth Pushparaj, Abian Sanchez.

---

## 📁 Data Standards: Why NetCDF?
The projects in this repository utilize [**NetCDF (Network Common Data Form)**](https://docs.unidata.ucar.edu/netcdf-c/current/), the industry standard for array-oriented scientific data. 

* **Multidimensional:** It allows for the storage of variables (temperature, pressure, solar irradiance) across 4D space-time coordinates ($x, y, z, t$).
* **Self-Describing:** Each file includes metadata (units, standard names, and coordinates), ensuring data integrity during high-throughput I/O.
* **Performance:** Optimized for large-scale parallel reads/writes on HPC clusters like [**NCAR Derecho**](https://www.cisl.ucar.edu/capabilities/derecho), facilitating the management of the **60 TB** dataset used in these simulations.

---

## 🚀 GCM Numerical Implementations & Core Projects

### 1. Bolometric Dimming and Climatic Response produced by a space-based Sunshade
* **Framework:** CESM GCM with the Community Atmospheric Model (CAM).
* **Implementation:** Hardcoded parameterization of uniform, non-spectral solar constant reductions (bolometric dimming) for baseline climate sensitivity testing.
* **Analytics Workflow:** Statistical analysis comparing bolometric forcing mechanisms on global stratospheric and surface temperature anomalies, as well as Arctic sea ice preservation.
* **Data Architecture:** Optimized the low-level Fortran I/O pipeline to ingest NetCDF4 parameters directly into the GCM core, maximizing computational efficiency to perform global sensitivity experiments, and ensuring seamless memory mapping between physical disk storage and the model’s numerical kernels.

### 2. Filter Analysis, Spectral Dimming and Climatic Response produced by a space-based Sunshade
* **Framework:** CESM with the Whole Atmosphere Community Climate Model (WACCM).
* **Implementation:** Numerical integration of a space-based (Lagrangian point L1) spectral filter sunshade dimming effect into the GCM radiative transfer core.
* **Analytics Workflow:** Developed spectral analysis pipelines to evaluate different wavelength bands radiation attenuations on the near infrared, focusing on different climate responses. Computed multidimensional climate anomaly diagnostics under the Shared Socioeconomic Pathways (SSP) framework **SSP2-4.5** future scenario.
* **Big Data Scale:** High-throughput I/O pipelines for **60 TB** of climate dataset output. Developed routines to ingest and transform NetCDF4 structures into multidimensional arrays within the Fortran model core on the NCAR Derecho HPC cluster, with subsequent statistical analysis via parallelized Python (Xarray/NumPy) workflows.

### 3. 4D Spatio-temporal Matrix Implementation and Simulations
* **Framework:** Modification of the solar forcing arrays inside the CESM GCM radiative transfer and the chemical modules.
* **Implementation:** Architected and embedded **4D numerical matrices** into the model's core to simulate the solar forcing dimming produced by a space-based sunshade located at the first Lagrangian point (L1). The dimming has a variability in time, latitude, longitude, and wavelength.
* **Analytics Workflow:** Implemented dynamic spatiotemporal distributions of dimming factors that scale the solar irradiance at the top of the atmosphere. Analysis of multi-variable climate responses to the localized radiative forcing over a long-term 30-year timeline [2035, 2065].
* **Core Skills:** Advanced Fortran modifications, NetCDF data creation and implementation on the global climate model, multidimensional coordinate mapping, and high-resolution 3D visualization.

---

## 🛠️ Production Stack
* **Languages:** Python (Xarray, NumPy, Pandas, Matplotlib), Fortran, Bash, SQL, IDL.
* **Data Standards:** NetCDF4, HDF5 (multidimensional arrays).
* **Infrastructure:** HPC (SLURM/PBS environments), Linux, Git, LaTeX.

---

## 👤 Contact & Professional Profiles
* **Current Position:** Postdoctoral Associate at **Cornell University**.
* **Education:** PhD in Astrophysics.
* **Academic Record:** [ORCID Profile](https://orcid.org/0000-0003-2254-5936) 
* **Research Portfolio:** [ResearchGate Profile](https://www.researchgate.net/profile/Illeana-Gomez-Leal-2)
* 📄 **Documentation:** [**Download Professional CV (PDF)**](cv_graphics.pdf)

---

> 📝 **Note:** This repository showcases specific technical implementations in **HPC and Climate Analytics**. For inquiries regarding my broader research in **Astrophysics and Climate Science**, please contact me via my ResearchGate profile or the email provided in my CV.
> 
> 🔒 **Privacy Note:** Full source code and configuration files are hosted in private repositories. Specific code samples (e.g., Python data pipelines or Fortran core modifications) are available upon request.
