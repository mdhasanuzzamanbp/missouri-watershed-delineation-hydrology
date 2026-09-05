# Hydrological Analysis of a Watershed in Western St. Louis County, Missouri, USA

## Executive Summary
<p align="justify">
I used QGIS to demonstrate a hydrological workflow for analysing the terrain, drainage network, and watershed structure of a selected study area in Missouri, USA. A digital elevation model (DEM) was processed in QGIS using Whitebox Workflows to prepare the terrain for hydrological modeling. 
</p>

The final output contains:
- Sub-basins
- Delineated Watershed
- Elevation Map
- Strahler Order
- Sediment Transport Index (STI)
- Slope

<p align="center">
<img width="4488" height="4960" alt="Final Map" src="https://github.com/user-attachments/assets/b5fad3bc-5c70-4711-bbd8-d091bb992f4a" />
</p>

## Project Workflow
- Prepared a DEM for hydrological analysis by removing artificial depressions.
- Extracted flow direction and flow accumulation from the conditioned DEM.
- Extracted a stream network using a 50,000 flow-accumulation threshold.
- Assigned Strahler stream orders to represent the drainage-network hierarchy.
- Delineated watersheds and sub-basins from selected outlet locations.
- Generated terrain and hydrological indicators, particularly slope and Sediment Transport Index (STI).
- Produced clear cartographic outputs suitable for watershed interpretation and GIS portfolio presentation.

<p align="center">
<img width="4113" height="1886" alt="Picture1" src="https://github.com/user-attachments/assets/4c45647c-ad15-4d82-9e0a-a2f0e2dbecc6" />
</p>
<br>

## Tools
**QGIS:** Whitebox workflows, Fill depression (Wang & Liu), Slope, Sediment Transport Index (STI), Extract streams, D8 pointer, D8 flow accumulation, Watershed, Subbasins, Strahler stream order, point <br>
**Microsoft Word:** Documentation

## Data Sources

| Dataset / Tool | Role | Usage |
|---|---|---|
| Digital Elevation Model (DEM)¹ | Primary elevation surface | Terrain and hydrological modelling |
| Watershed Boundary Dataset (WBD)² | Reference hydrographic boundaries | Study-area and watershed context |

¹ [USGS EarthExplorer](https://earthexplorer.usgs.gov/)  
² [USGS National Map](https://apps.nationalmap.gov/)

## Resuts
### DEM Elevation & Slope
At first, DEM data were downloaded, and the elevations were calculated to characterize the topographic variation across the study area. Elevation values range from approximately 123 to 298 m, showing the variation of the terrain. Moreover, slope analysis was also conducted  to quantify terrain steepness. The resulting raster highlights the contrast between relatively flat floodplain and steeper upland terrain. Slope is an important conditioning factor for runoff concentration, erosion, and sediment transport. Around the floodplain zone, the slope was nearly 0o where some regions it reached upto 39o. Then it was processed for further hydrological modelling.  Fill depression (Wang & Liu) was used to remove artificial pits and fill the sinks. The processed DEM was then used as the primary elevation input for further hydrological analysis. 

### Subbasins and Watershed Structure
With the filled DEM, the downslope direction of surface flow was identified with the D8 pointer tool. With flow direction data, flow accumulation and stream extraction were also performed. To extract the stream network, flow direction data was used with a threshold of 50,000. The reason of using the threshold was to retain only larger drainage paths. Finally, with all the datasets, watershed and subbasin analyses were conducted. They show a connected hierarchy of tributaries toward the main drainage outlets. 

### Strahler Stream Ordering
The extracted drainage network was classified using the Strahler stream-order concept. To extract this, the Strahler order tool was used with flow direction datasets. First-order streams represent the smallest mapped headwater channels. When two streams of the same order meet, the downstream segment increases by one order. On the other hand, when different orders meet, the downstream segment retains the higher order. This provides a hierarchical description of drainage-network structure. 

### Sediment Transport Index (STI)
The STI was extracted from specific catchment area (SCA) and slope to identify spatial variations in the relative potential for sediment transport. Areas with higher STI values indicate locations where the combination of contributing area and terrain slope may promote greater sediment-transport potential.

## Limitations
- Stream extraction depends strongly on the selected flow-accumulation threshold.
- The analysis does not by itself model rainfall, soil infiltration, land cover, hydraulic capacity, or flood depth.
- Independent hydrographic data can differ from DEM-derived drainage 

## Recommendation
- Use different thresholds for specific levels of stream extraction and  Strahler stream order.
- Identify more outlet points for smaller-scale study.
- Calculate the Stream Power Index.
