# Blue Carbon Ecosystems Restoration Tool User Manual


## Table of Contents
1. [Introduction](#introduction)
2. [Abstarct From Paper](#abstract-from-paper)
3. [System Requirements](#system-requirements)
4. [Installation](#installation)
5. [Data Requirements](#data-requirements)
6. [Tool Setup](#tool-setup)
7. [Running the Tool](#running-the-tool)
8. [Interpreting Results](#interpreting-results)
9. [Troubleshooting](#troubleshooting)
10. [Contributing](#contributing)

## Introduction

The Blue Carbon Ecosystem (BCE) Restoration Tool is a Geographic Information System (GIS)-based multi-criteria decision support tool designed to identify suitable areas for BCE restoration. It focuses on mangroves, saltmarshes, and seagrasses, integrating spatial data on current and historical BCE distribution, coastal geomorphology, hydrodynamics, and land tenure.

## Abstract From Paper
Blue carbon ecosystems (BCEs), such as mangroves, saltmarshes, and seagrasses, are important nature-based solutions for climate change mitigation and adaptation but are threatened by degradation. Effective BCE restoration requires strategic planning and site selection to optimise outcomes. We developed a Geographic Information System (GIS)-based multi-criteria decision support tool to identify suitable areas for BCE restoration along the 2,512 km-long coastline of Victoria, Australia. High-resolution spatial data on BCE distribution, coastal geomorphology, hydrodynamics, and land tenure were integrated into a flexible spatial model that distinguishes between passive and active restoration suitability. The tool was applied to identify high-priority locations for mangrove, saltmarsh, and seagrass restoration across different scenarios. Results indicate substantial potential for BCE restoration in Victoria, with 33,253 ha of suitable area identified, mostly (>97%) on public land, which aligned with the selection criteria used in the tool. Restoration opportunities are concentrated in bays and estuaries where historical losses have been significant. The mapped outputs provide a decision-support framework for regional restoration planning, while the tool itself can be adapted to other geographies.

## System Requirements

- ArcGIS Pro 3.0.1 or later
- Python 3.x (included with ArcGIS Pro)
- Minimum 8GB RAM (16GB or more recommended for large datasets)
- Storage space dependent on the size of your input datasets

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/your-repo/bce-restoration-tool.git
   ```
2. Open ArcGIS Pro and create a new project
3. In the Catalog pane, right-click on Toolboxes and select "Add Toolbox"
4. Navigate to the cloned repository and select the BCE Restoration Tool toolbox

## Data Requirements

The tool requires the following spatial data layers:

1. **Current BCE Distribution**
   - Format: Vector (polygon)
   - Resolution: 1-5 m
   - Attributes: BCE type (mangrove, saltmarsh, seagrass)

2. **Historic BCE Distribution** (for mangroves and saltmarshes)
   - Format: Vector (polygon)
   - Attributes: BCE type

3. **Coastal Erosion Sensitivity**
   - Format: Vector (line or polygon)
   - Resolution: 50 m segments
   - Attributes: Erosion sensitivity category

4. **Shoreline Substrate Erodibility**
   - Format: Vector (line or polygon)
   - Resolution: 50 m segments
   - Attributes: Substrate erodibility category

5. **Significant Wave Height**
   - Format: Vector (line or polygon)
   - Resolution: 50 m segments
   - Attributes: Wave height category

6. **Land Tenure**
   - Format: Vector (polygon)
   - Resolution: Parcel-scale (~1:500)
   - Attributes: Land ownership category

All spatial data should be in the same coordinate system, preferably a projected coordinate system appropriate for your study area.

## Tool Setup

1. Open your ArcGIS Pro project
2. In the Catalog pane, expand the BCE Restoration Tool toolbox
3. Double-click on the BCE Restoration Tool to open it

## Running the Tool

1. **Select target BCE type**: Choose mangrove, saltmarsh, or seagrass
2. **Set buffer distance**: Enter the distance to buffer existing BCE habitats (e.g., 100 m)
3. **Choose restoration scenario**:
   - Sheltered Passive Restoration
   - Moderate Passive Restoration
   - Sheltered Active Restoration
   - Moderate Active Restoration
4. **Input data layers**: Select the required input layers from your project
5. **Set output location**: Choose where to save the results
6. **Run the tool**: Click "Run" and wait for the process to complete

## Interpreting Results

The tool generates two main outputs:

1. **Potential restoration areas map**: Shows suitable areas symbolized by BCE type and restoration approach (passive/active)
2. **Summary table**: Lists total restorable area by BCE type, suitability class, and land tenure category

Additionally, the tool calculates the distance from each potential restoration site to the nearest existing BCE habitats.

## Troubleshooting

- Ensure all input data are in the same coordinate system
- Check that input layers have the required attributes
- For large datasets, try running the tool on a subset of the data first
- If the tool crashes, try increasing the available memory for ArcGIS Pro

## Contributing

We welcome contributions to improve the BCE Restoration Tool. Please submit issues and pull requests through the GitHub repository.

When contributing, please:
- Follow the existing code style
- Add comments to your code
- Update the documentation if you make changes to the tool's functionality
- Test your changes thoroughly before submitting a pull request

## Contributing
We welcome contributions to improve the BCE Restoration Tool. Please feel free to submit issues or pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Citation
If you use this tool in your research, please cite:
[Include your paper's citation here once published]

## Contact
[Your Name] - [Your Email]

Project Link: [https://github.com/yourusername/BCE-Restoration-Tool](https://github.com/yourusername/BCE-Restoration-Tool)
