# Hydrological Analysis of a Watershed in Western St. Louis County, Missouri, USA

## Executive Summary
I used QGIS to demonstrate a hydrological workflow for analysing the terrain, drainage network, and watershed structure of a selected study area in Missouri, USA. A digital elevation model (DEM) was processed in QGIS using Whitebox Workflows to prepare the terrain for hydrological modeling. 

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

Workflow
Prepared a DEM for hydrological analysis by removing artificial depressions.
Extracted flow direction and flow accumulation from the conditioned DEM.
Extracted a stream network using a 50,000 flow-accumulation threshold.
Assigned Strahler stream orders to represent the drainage-network hierarchy.
Delineated watersheds and sub-basins from selected outlet locations.
Generated terrain and hydrological indicators, particularly slope and Sediment Transport Index (STI).
Produce clear cartographic outputs suitable for watershed interpretation and GIS portfolio presentation.




Tools
QGIS: Whitebox workflows, Fill depression (Wang & Liu), Slope, Sediment Transport Index (STI), Extract streams, D8 pointer, D8 flow accumulation, Watershed, Subbasins, Strahler stream order, point
Microsoft Word: Documentation


Project Workflow
