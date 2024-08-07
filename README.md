# Blue Carbon Ecosystems Restoration Tool User Manual


## Table of Contents
1. [Introduction](#introduction)
2. [System Requirements](#system-requirements)
3. [Installation](#installation)
4. [Data Requirements](#data-requirements)
5. [Running the Tool](#running-the-tool)
6. [Interpreting Results](#interpreting-results)
7. [Troubleshooting](#troubleshooting)
8. [Contributing](#contributing)
9. [Citation](#citation)

## Introduction

The Blue Carbon Ecosystem (BCE) Restoration Tool is an innovative, Geographic Information System (GIS)-based multi-criteria decision support tool designed to identify suitable areas for BCE restoration. Developed to address the critical need for strategic planning in coastal ecosystem restoration, this tool focuses on three key blue carbon ecosystems: mangroves, saltmarshes, and seagrasses.

By integrating high-resolution spatial data on current and historical BCE distribution, coastal geomorphology, hydrodynamics, and land tenure, the BCE Restoration Tool provides a comprehensive framework for assessing restoration potential. Its unique strength lies in its ability to distinguish between passive and active restoration suitability, offering nuanced insights for restoration planning and resource allocation.

Initially developed and tested along the 2,512 km coastline of Victoria, Australia, this tool demonstrates significant potential for identifying restoration opportunities. In our case study, we identified 33,253 hectares of suitable area for BCE restoration, with the majority located on public land. These findings underscore the tool's capacity to inform large-scale restoration efforts and contribute to climate change mitigation and adaptation strategies.

Importantly, while the tool was developed using data from Victoria, its methodology and framework are designed to be globally applicable. The data requirements and analysis approach can be adapted to other coastal regions worldwide, making this tool a valuable resource for restoration practitioners, environmental managers, and policymakers across different geographical contexts.

We have developed this spatial tool to highlight areas of coastlines that have characteristics and history that may be suitable for different types of restoration. As with most large-scale spatial assessments, we strongly recommend ground-truthing and site-specific assessments to validate and refine potential restoration sites identified by the tool.

### Global Applicability

It's important to highlight that while the example data provided with this tool is specific to the Victorian coastline in Australia, the methodology and data structure can be applied globally. Researchers and practitioners from other regions can use this tool by substituting the Victorian data with equivalent datasets for their area of interest. This flexibility allows for the identification of blue carbon restoration opportunities in diverse coastal environments around the world.

When adapting the tool to other regions:
1. Ensure that you have similar data layers (current and historical BCE distribution, coastal geomorphology, hydrodynamics, and land tenure) for your area of interest.
2. Adjust the classification schemes for variables like wave height, erosion sensitivity, and substrate types to match the characteristics of your local coastal environment.
3. Consider local ecological, social, and economic factors that might influence restoration suitability in your region.

By providing a transferable framework, this tool aims to support global efforts in blue carbon ecosystem restoration, contributing to climate change mitigation and coastal resilience worldwide.

## System Requirements

- ArcGIS Pro 3.0.1 or later
- Python 3.x (included with ArcGIS Pro)
- Storage space dependent on the size of your input datasets

## Installation

The BCE Restoration Tool can be installed and used in two ways: as a complete package with example data for Victoria, Australia, or as a standalone toolbox for use with your own data.

### Option 1: Complete Package for Victoria, Australia

This option is ideal if you want to explore the tool with pre-loaded data or use the Victorian dataset as a template for your own project.

1. Go to the GitHub repository: [https://github.com/NuytsSiegmund/BlueCarbon_RestorationTool](https://github.com/NuytsSiegmund/BlueCarbon_RestorationTool/tree/main/BCE_RestorationTool)
2. Download the Package Project file: `BCE_RestorationTool.ppkx`
3. Navigate to your downloaded file and double-click on `BCE_RestorationTool.ppkx`
4. ArcGIS Pro will open with all necessary data and toolboxes pre-loaded

### Option 2: Standalone Toolbox for Custom Data

This option is best if you want to use the tool with your own data from a different region.

1. Go to the GitHub repository: https://github.com/NuytsSiegmund/BlueCarbon_RestorationTool/blob/main/BCE_RestorationTool.atbx
2. Download the toolbox file: `BCE_RestorationTool.atbx`
3. Open ArcGIS Pro and create a new project or open an existing one
4. In the Catalog pane, right-click on Toolboxes and select "Add Toolbox"
5. Navigate to the downloaded `BCE_RestorationTool.atbx` file and select it

### Post-Installation Steps

After installation using either method:

1. Ensure that all required data layers are present and properly formatted (see [Data Requirements](#data-requirements) section)
2. If using your own data, make sure it's in the same coordinate system as specified in the tool
3. Familiarize yourself with the tool interface and parameters before running analyses

Remember, while the packaged project provides a ready-to-use example for Victoria, the methodology can be applied globally. When using your own data, you may need to adjust certain parameters or classification schemes to better suit your local coastal environment.

## Data Requirements

The tool requires the following spatial data layers:

1. **Current BCE Distribution**
   - Format: Vector (polygon)
   - Recommended Resolution: 1-5 m
   - Attributes: BCE type (mangrove, saltmarsh, seagrass)

2. **Historic BCE Distribution** 
   - Format: Vector (polygon)
   - Attributes: BCE type

3. **Coastal Erosion Sensitivity**
   - Format: Vector (line)
   - Recommended Resolution: 50 m segments
   - Attributes: Erosion sensitivity category

4. **Shoreline Substrate Erodibility**
   - Format: Vector (line)
   - Recommended Resolution: 50 m segments
   - Attributes: Substrate erodibility category

5. **Significant Wave Height**
   - Format: Vector (line)
   - Recommended Resolution: 50 m segments
   - Attributes: Wave height category

6. **Land Tenure**
   - Format: Vector (Line or polygon)
   - Recommended Resolution: Parcel-scale (~1:500)
   - Attributes: Land ownership category

All spatial data should be in the same coordinate system, preferably a projected coordinate system appropriate for your study area.

## Running the Tool

1. **Select target BCE type**: Choose mangrove, saltmarsh, or seagrass
2. **Set buffer distance**: Enter the distance to buffer existing BCE habitats (e.g., 250 m)
3. **Take into account historical vegetation**: Choose if you want to focus specifically on areas that historically had vegetation
4. **Select Wave Height Category**: Choose Very low (<0.4 m), Low (0.4 – 1 m), Moderate (1 – 1.5 m), High (1.5 – 2.25 m), or Very high (> 2.25 m) Significant wave height
5. **Select Erodibility**: Choose Rapid accretion, Accretion, Stable, Erosion, or Rapid erosion
6. **Select Substrate**: Choose Artificial, Hard rock, Soft rock, Soft sediment, or Sandy
7. **Land Tenure**: Choose Private, Public, or both
8. **Set output location**: Choose where to save the results
9. **Run the tool**: Click "Run" and wait for the process to complete

## Interpreting Results

The tool generates two main outputs:

1. **Potential restoration areas map**: Shows suitable areas symbolised by chosen BCE type chosen coastal attributes
2. **Summary table**: Lists total restorable area by BCE type, suitability class, and land tenure category

Additionally, the tool calculates the distance from each potential restoration site to the nearest existing BCE habitats.

## Troubleshooting

- Ensure all input data are in the same coordinate system
- Ensure no "<Null>" data is in the data
- Check that input layers have the required attributes
- Data examples are available for Victorian coastline in Australia

## Contributing

We welcome contributions to improve the BCE Restoration Tool. Please feel free to submit issues or pull requests. For major changes, please open an issue first to discuss what you would like to change.

When contributing, please:
- Follow the existing code style
- Update the documentation if you make changes to the tool's functionality
- Test your changes thoroughly before submitting a pull request

## Citation
If you use this tool in your research, please cite:

Nuyts, S., Duarte de Paula Costa, M., Macreadie, P. I., & Trevathan-Tackett, S. M. (2024). A decision support tool to help identify blue carbon sites for restoration. Journal of Environmental Management, 367, 122006. https://doi.org/https://doi.org/10.1016/j.jenvman.2024.122006 

