***

# OGDSS-BigData: Open Geospatial Data Sharing System

[![FOSS4G-2026](https://img.shields.io/badge/FOSS4G-2026_Academic_Track-blue)](https://2026.foss4g.org)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Reproducibility](https://img.shields.io/badge/Reproducibility-Docker_Verified-green)](#-one-click-reproducibility)

## 📌 Project Overview
This repository contains the framework and source code for the paper:  
**"Open Geospatial Data Sharing Systems for Big Data Analytics: A Framework for Scalable, Reproducible, and Collaborative Research"**

Submitted to the **FOSS4G 2026 Academic Track** (Tokyo, Japan).

This project addresses the "interoperability gap" in geospatial Big Data by implementing a **Cloud-Native Geospatial (CNG)** architecture. It demonstrates how institutions in resource-constrained environments, such as the **Jinka Regional Veterinary Laboratory (Ethiopia)**, can leverage global Big Data initiatives (such as **Japan's Project PLATEAU** and **JAXA**) to solve local and transboundary challenges.

## 🚀 One-Click Reproducibility
In accordance with the FOSS4G commitment to open science, this research is fully containerized. Reviewers can instantiate the entire analytical stack with a single command.

### Prerequisites
- Docker
- Docker-Compose

### Quick Start
```bash
# Clone the repository
git clone https://github.com/bayillag/OGDSS-BigData.git
cd OGDSS-BigData

# Start the FOSS4G stack (PostGIS, pygeoapi, JupyterHub)
docker-compose up -d
```
*   **Jupyter Analytics Environment:** `http://localhost:8888` (Token: `foss4g`)
*   **OGC API Features Service:** `http://localhost:8000`

## 🛠️ The FOSS4G Stack
The OGDSS framework is built entirely on OSGeo-aligned and open-source technologies:
- **Storage:** Cloud-Optimized GeoTIFFs (COG), GeoParquet, and Zarr.
- **Cataloging:** SpatioTemporal Asset Catalog (STAC) via `pygeoapi`.
- **Database:** PostGIS 3.4 / PostgreSQL 16.
- **Analytics:** Distributed processing using `Dask-Geo` and `Apache Sedona`.
- **Mediation:** OGC API (Features, Tiles, Processes).

## 🌏 Case Studies & Regional Synergies
This framework is validated through three multi-source case studies:
1.  **Tokyo Urban Resilience (Japan):** Scalable vector processing of massive 3D CityGML models from **Project PLATEAU**.
2.  **Mekong Basin (SE Asia):** Transboundary flood detection using **JAXA ALOS-2 SAR** L-band data via cloud-native streams.
3.  **One Health Surveillance (East Africa):** Zoonotic risk modeling in South Ethiopia, integrating climate reanalysis (ERA5) with laboratory epidemiological records.

## 📂 Repository Structure
- `notebooks/`: Reproducible Jupyter Notebooks for each case study.
- `config/`: Configuration files for `pygeoapi` and PostGIS initialization.
- `src/`: Core Python modules for STAC ingestion and distributed analytics.
- `docker-compose.yml`: Orchestration for the local development environment.

## 📜 Citation
If you use this framework or the associated research in your work, please cite it as follows:
> Geda, B. (2026). Open Geospatial Data Sharing Systems for Big Data Analytics: A Framework for Scalable, Reproducible, and Collaborative Research. *Proceedings of FOSS4G 2026 Academic Track*, Tokyo, Japan.

## ⚖️ License
- **Software:** All source code is released under the **GNU GPL v3.0**.
- **Documentation & Data:** Metadata, notebooks, and visuals are released under **CC BY 4.0**.

---
**Contact:** Bayilla Geda (bayillag@gmail.com)  
**Affiliation:** Jinka Regional Veterinary Laboratory, South Ethiopia Regional State, Ethiopia.
