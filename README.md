# MMG-5GeoInstruct

<p align="center">
  <img src="assets/MMG-5GeoInstruct_overview.png" width="95%">
</p>

<p align="center">
  <b>MMG-5GeoInstruct: A Multimodal Geological Instruction Dataset for Geospatial Vision-Language Learning</b>
</p>

MMG-5GeoInstruct is a multimodal geospatial image-text dataset designed to connect heterogeneous Earth observation measurements with explicit geological semantics. It extends the MMG-5 observation base by introducing structured geological language annotations derived from multimodal physical evidence and domain knowledge.

The dataset contains **119,080 spatially aligned image-text pairs** distributed across **18 geographic sites**. Each spatial sample includes five aligned Earth observation products, including **RGB, SWIR, SAR, DEM, and LULC**, together with structured annotations describing **terrain, materials, anomalies, and natural-language captions**.

MMG-5GeoInstruct is developed in conjunction with our work:

> **<Exact Paper Title>**  
> <Authors>  
> <Journal / Conference / Preprint, Year>

Paper: `<Paper URL>`  
Dataset: `<Dataset Download URL>`

---

## Highlights

- **119,080** spatially aligned multimodal image-text pairs.
- **5 aligned Earth observation modalities:** RGB, SWIR, SAR, DEM, and LULC.
- **18 geographically distributed sites** covering diverse terrain and geological environments.
- Structured geological annotations covering **terrain, material, anomaly, and caption** information.
- **80,643 samples (67.72%)** contain explicit anomaly-related descriptions.
- Geological text is constructed from both **multimodal physical evidence** and **curated geological knowledge**.
- All observations are spatially aligned to a common **10 m grid**.

---

## Dataset Overview

| Property | MMG-5GeoInstruct |
| --- | --- |
| Spatial samples | 119,080 |
| Geographic sites | 18 |
| Aligned observations | RGB, SWIR, SAR, DEM, LULC |
| Final spatial grid | 10 m |
| Text fields | Terrain, Material, Anomalies, Caption |
| Anomaly-related samples | 80,643 (67.72%) |
| Samples without explicit anomalies | 38,437 |
| Terrain expressions | 17 |
| Material expressions | 2,916 |
| Anomaly expressions | 266 |

---

## Multimodal Earth Observation Data

MMG-5GeoInstruct integrates complementary observations of the same geographic locations. Each modality provides different physical or semantic information about the Earth's surface.

| Modality | Data Source | Observation | Native Resolution |
| --- | --- | --- | --- |
| RGB | Sentinel-2 MSI L2A | B4 / B3 / B2 | 10 m |
| SWIR | Sentinel-2 MSI L2A | B12 | 20 m |
| SAR | Sentinel-1 C-SAR GRD | VV, IW mode | ~20 × 22 m |
| DEM | NASA SRTM V3 | Elevation | ~30 m |
| LULC | ESA WorldCover v100 | Land-use / land-cover | 10 m |

All modalities are spatially aligned to a common 10 m grid. Detailed acquisition, preprocessing, registration, and geometric quality control follow the MMG-5 observation construction procedure described in our previous work.

---

## Geological Text Construction

The geological annotations are generated through a two-stage procedure that connects local multimodal observations with geological knowledge.

### Stage I: Physics-Derived Multimodal Evidence Extraction

Quantitative evidence is extracted from RGB, SWIR, SAR, and DEM observations to characterize surface appearance, spectral response, microwave scattering, and terrain morphology. LULC information is retained as semantic surface context.

### Stage II: Geological Knowledge-Constrained Semantic Synthesis

The extracted physical evidence is combined with curated geological knowledge to construct structured geological descriptions. Domain references include:

- FAO/ISRIC SOTER for terrain interpretation
- FAO Land Cover Classification System for surface semantics
- USGS Spectral Library for material-related spectral interpretation
- Regional geological resources such as Macrostrat
- Additional regional geological knowledge for the 18 geographic subsets

The resulting annotation contains four structured fields:

```text
terrain
material
anomalies
caption
