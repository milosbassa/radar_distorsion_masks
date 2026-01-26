# SAR Geometric Distortion Masks and Spatial Distribution Dataset

This repository provides a publicly available dataset of SAR geometric distortion products derived from Sentinel-1 imagery. The dataset includes distortion masks, spatial distribution maps, zonal statistics outputs, and supplementary visualization layers used in the associated scientific publication.

The dataset was generated using ESA SNAP software and SRTM 1 arc-second DEM and is intended to support research on SAR geometric distortions, terrain effects, and spatial analysis of layover and shadow phenomena.

---

## Dataset Access

The full dataset can be downloaded from:

➡ Dataset download link (Release archive):  
[ADD RELEASE DOWNLOAD LINK HERE]

---

## Dataset Content

The repository contains the following data products:

### 1. Distortion Mask Rasters (18 files)

A total of 18 raster masks are provided:

- 6 original distortion mask rasters  
- 6 masks expanded by a 2-pixel buffer  
- 6 masks expanded by a 5-pixel buffer  

These layers represent different spatial extents of SAR geometric distortions to support sensitivity analysis and uncertainty assessment.

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
- 1 raster visualization showing sample distortion areas used in the publication figures  

These layers are intended for visualization, quality control, and reproducibility of the published results.

---

### 4. Tabular Data (2 tables)

Two tables used in the scientific analysis are provided:

- Table defining processing parameters and distortion classes  
- Table summarizing statistical results used in the manuscript  

The tables are provided in standard tabular format for easy reuse and verification.

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

Bassa, M. (2026). SAR Geometric Distortion Masks and Spatial Distribution Dataset (Version 1.0.0). GitHub repository.  
https://github.com/milosbassa/radar_distorsion_masks

---

## License

This dataset is distributed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).  
Users are free to share and adapt the data, provided appropriate credit is given.

---

## Contact

For questions or additional information regarding the dataset, please contact the repository owner via GitHub.
