# SAR Geometric Distortion Masks and Spatial Distribution Dataset

[![DOI](https://zenodo.org/badge/1132104713.svg)](https://doi.org/10.5281/zenodo.18380989)

This repository provides a publicly available dataset of SAR geometric distortion (Layover and Shadow) products derived from Sentinel-1 imagery. The dataset includes distortion masks, spatial distribution maps (onal statistics outputs), and supplementary visualization layers used in the associated scientific publication.

The dataset was generated using ESA SNAP software and SRTM 1 arc-second DEM and is intended to support research on SAR geometric distortions, terrain effects, and spatial analysis of layover and shadow phenomena.

---

## Dataset Access

The full dataset can be downloaded from:

➡ Dataset download link (Release archive):  

Raster distorsion masks:

https://github.com/milosbassa/radar_distorsion_masks/blob/1647f5f05ddea58566b743fd3bdacc3a79b79b4e/Raster_results.rar](https://github.com/milosbassa/radar_distorsion_masks/blob/1a91b72bcb242dc2c2329828c539737ff77c4a09/Dataset%20-%20Raster%20masks.rar

Zonal statistics overview:

*main*

https://github.com/milosbassa/radar_distorsion_masks/blob/1a91b72bcb242dc2c2329828c539737ff77c4a09/Dataset%20-%20Zonal%20statistic%20(Mean).rar

*sum*

https://github.com/milosbassa/radar_distorsion_masks/blob/1a91b72bcb242dc2c2329828c539737ff77c4a09/Dataset%20-%20Zonal%20statistics%20(Sum).rar

---

## Dataset Content

The repository contains the following data products:

### 1. Distortion Mask Rasters (18 files)

For each SAR geometric distortion type (layover, shadow, and their combination), both ascending and descending orbit acquisition geometries were considered. This resulted in a total of six primary distortion mask types:

- layover in ascending orbit geometry,

- layover in descending orbit geometry,

- shadow in ascending orbit geometry,

- shadow in descending orbit geometry,

- combined layover and shadow in ascending orbit geometry,

- combined layover and shadow in descending orbit geometry.

For each of these six distortion types, an original binary raster mask was generated to directly identify pixels affected by the corresponding geometric distortion. In addition to the original masks, extended versions were produced to account for spatial uncertainty related to imaging geometry, terrain representation errors in the digital elevation model, and mixed-pixel effects near distortion boundaries.

Specifically, three variants were created for each distortion type:

- the original mask without spatial expansion,

- a mask expanded by a 2-pixel buffer,

- a mask expanded by a 5-pixel buffer.

This resulted in a total of 18 raster masks (6 distortion types × 3 variants), enabling flexible sensitivity analysis of geometric distortion impacts depending on the selected spatial tolerance.

Sample of descending radar shadow mask generation and pixel-based spatial expansion in mountainous terrain

<img width="379" height="378" alt="image" src="https://github.com/user-attachments/assets/fb7e6c44-3d87-46ae-80c8-5d107af1a05a" />

The upper-left panel shows the local terrain morphology, while the upper-right panel illustrates the original distortion mask. In this mask, darker red pixel values indicate shadow areas that spatially overlap with shadow occurrences detected in other SAR acquisitions, whereas brighter red pixels represent isolated distortion instances specific to the analyzed scene

---

### 2. Spatial Distribution Maps (12 files)

Spatial statistics derived from zonal analysis:

- 6 mean zonal statistics maps  
- 6 sum zonal statistics maps  

These rasters describe the spatial frequency and intensity of distortion occurrence across the study area.

---

### 3. Supplementary Visualization Layers

The dataset also includes:

- 1 raster showing Sentinel-1 acquisition footprint coverage

![Asc   Desc](https://github.com/user-attachments/assets/e5533655-cd01-486f-9b74-1c06951dec0b)

- 1 raster visualization showing sample distortion areas used in the publication figures  

Mean-based zonal statistics of radar distortions across Serbia. Top row: ascending, bottom row: descending; columns (left to right): layover, shadow, combined.

<img width="5216" height="3848" alt="mean" src="https://github.com/user-attachments/assets/afba9d33-a319-408b-8f62-83d5fee79834" />

Sum-based zonal statistics of radar distortions across Serbia. Top row: ascending, bottom row: descending; columns (left to right): layover, shadow, combined.

<img width="5760" height="3920" alt="sum" src="https://github.com/user-attachments/assets/315762d2-cc24-425b-adcd-73d06fda0b23" />

These layers are intended for visualization of the published results.

---

### 4. Sentinel 1 imagery tables

Two tables used in the scientific analysis are provided:

- Table 1.	Technical characteristics and metadata of the Ascending SAR imagery dataset.

<img width="1027" height="611" alt="Asc" src="https://github.com/user-attachments/assets/68a79043-a368-44f2-8a1a-71dc822de338" />

- Table 2.	Technical characteristics and metadata of the Descending SAR imagery dataset.

<img width="1063" height="617" alt="Desc" src="https://github.com/user-attachments/assets/1752f8e2-f7ec-45a4-a7e4-0ec9bb9528d7" />

---

## Data Format and Spatial Reference

All raster layers share the following properties:

- Format: GeoTIFF  
- Coordinate Reference System: WGS 1984 (EPSG:4326)  
- Spatial resolution: 10 m  
- NoData value: -9999  

---

## Processing Overview

The dataset was generated from Sentinel-1 SAR imagery using the ESA SNAP processing chain. The workflow included precise orbit correction (Precise Orbit Ephemerides), deburst processing, SAR simulation, terrain correction, and distortion mask generation using the 2-pass layover and shadow detection algorithm. SRTM 1 arc-second DEM (HGT format) was used as the reference elevation dataset.

---

## How to Use the Dataset

The GeoTIFF raster layers can be directly imported into standard GIS software such as QGIS or ArcGIS.

Example use cases include:

- Overlay distortion masks with land cover or infrastructure layers to assess terrain-induced SAR distortions  
- Use expanded masks (2 px and 5 px buffers) for uncertainty or sensitivity analysis  
- Analyze spatial distribution maps to identify regions with frequent layover or shadow effects  
- Combine zonal statistics layers with administrative or environmental units for regional analysis  

All tabular data can be loaded into spreadsheet software or statistical environments such as Python or R.

---

## Citation

If you use this dataset in your research, please cite it as:

Basaric, M. (2026). SAR Geometric Distortion Masks and Spatial Distribution Dataset (Version 1.0.0). GitHub repository.  
https://github.com/milosbassa/radar_distorsion_masks

---

## License

This dataset is distributed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).  
Users are free to share and adapt the data, provided appropriate credit is given.

---

## Contact

For questions or additional information regarding the dataset, please contact the repository owner via GitHub.
