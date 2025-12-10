# GlobalBuildingAtlas

## Introduction
In this project, we provide the level of detail 1 (LoD1) data of buildings across the globe.

A overview of the dataset is illustrated bellow:

<img src="figures/overview.png" width="800">


## Access to the Data
### Web Feature Service (WFS)
A WFS is provided so that one can access the data using other websites or GIS softwares such as QGIS and ArcGIS.

Url: `https://tubvsig-so2sat-vm1.srv.mwn.de/geoserver/ows?`

### Web Viewer
A web interface for viewing the data is available at: [website](https://tubvsig-so2sat-vm1.srv.mwn.de)

Note: Over the past few days, our web viewer has received nearly 280,000 access requests. Due to this unusually high traffic, some data may not load completely, which may result in a significant portion of buildings not being displayed.

### Full Data Download
The full data can be downloaded from [mediaTUM](https://mediatum.ub.tum.de/1782307)

## Development Code
### Global Building Polygon Generation using Satellite Data (Sec. 4.3)
For codes related to building map extraction, regularization, polygonization, and simplification, i.e., generating building polygons from satellite images (Sec. 4.3.2, Sec. 4.3.3, and Sec. 4.3.4), please refer to `./im2bf`.

### Global Building Height Estimation (Sec. 4.4)
1. For codes related to monocular height estimation using HTC-DC Net (Sec. 4.4.2), please refer to `./im2bh`.
2. For codes related to the global inference and uncertainty quantification (Sec. 4.4.3), please refer to `./infer_height`

### Global LoD1 Building Model Generation (Sec. 4.5)
1. For codes related to quality-guided building polygon fusion (Sec. 4.5.1), please refer to `./fuse_bf`.
2. For codes related to LoD1 building model generation (Sec. 4.5.2), please refer to `./make_lod1`.

## Visualization Code
For codes to reproduce the plots in the manuscript, please refer to `./make_plots`.

## Code License
MIT with Commons Clause (no commercial use allowed). See [LICENSE](https://github.com/zhu-xlab/GlobalBuildingAtlas/blob/main/LICENSE).

## How to cite
If you find this dataset helpful in your work, please cite the following paper.
```
@Article{essd-17-6647-2025,
AUTHOR = {Zhu, X. X. and Chen, S. and Zhang, F. and Shi, Y. and Wang, Y.},
TITLE = {GlobalBuildingAtlas: an open global and complete dataset of building polygons, heights and LoD1 3D models},
JOURNAL = {Earth System Science Data},
VOLUME = {17},
YEAR = {2025},
NUMBER = {12},
PAGES = {6647--6668},
URL = {https://essd.copernicus.org/articles/17/6647/2025/},
DOI = {10.5194/essd-17-6647-2025}
}
```
