# MMG-5GeoInstruct

<p align="center">
  <img src="assets/MMG-5GeoInstruct.png" width="90%">
</p>

MMG-5GeoInstruct is a multimodal geological vision-language dataset designed for unified Earth observation understanding. It contains 119,080 spatially aligned image-text pairs across 18 geographic sites, integrating RGB, SWIR, SAR, DEM, and LULC observations with structured geological annotations covering terrain, materials, anomalies, and descriptive captions. The dataset is designed to provide multimodal physical observations together with geological language information for geospatial vision-language learning.

## Dataset Statistics

| Item | Description |
| --- | --- |
| Number of samples | 119,080 |
| Geographic sites | 18 |
| Modalities | RGB, SWIR, SAR, DEM, LULC |
| Spatial grid | 10 m |
| Annotation fields | Terrain, Material, Anomalies, Caption |
| Samples with anomaly descriptions | 80,643 (67.72%) |
| Terrain expressions | 17 |
| Material expressions | 2,916 |
| Anomaly expressions | 266 |
| Caption length | 16--50 words |
| Mean caption length | 27.43 words |

## Paper

**GeoPlex: A Unified Foundation Model for Multi-Modal Earth Observation Tasks via Flow Matching**

**Authors:** Wenzheng Zhang, Zhanlong Chen  
**Affiliation:** China University of Geosciences (Wuhan)

If you use MMG-5GeoInstruct in your research, please cite:

```bibtex
@article{zhang2026geoplex,
  title   = {GeoPlex: A Unified Foundation Model for Multi-Modal Earth Observation Tasks via Flow Matching},
  author  = {Zhang, Wenzheng and Chen, Zhanlong},
  journal = {Under Review},
  year    = {2026}
}
