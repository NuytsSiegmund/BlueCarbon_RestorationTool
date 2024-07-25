# BCE Restoration Tool

## Abstract
Blue carbon ecosystems (BCEs), such as mangroves, saltmarshes, and seagrasses, are important nature-based solutions for climate change mitigation and adaptation but are threatened by degradation. Effective BCE restoration requires strategic planning and site selection to optimise outcomes. We developed a Geographic Information System (GIS)-based multi-criteria decision support tool to identify suitable areas for BCE restoration along the 2,512 km-long coastline of Victoria, Australia. High-resolution spatial data on BCE distribution, coastal geomorphology, hydrodynamics, and land tenure were integrated into a flexible spatial model that distinguishes between passive and active restoration suitability. The tool was applied to identify high-priority locations for mangrove, saltmarsh, and seagrass restoration across different scenarios. Results indicate substantial potential for BCE restoration in Victoria, with 33,253 ha of suitable area identified, mostly (>97%) on public land, which aligned with the selection criteria used in the tool. Restoration opportunities are concentrated in bays and estuaries where historical losses have been significant. The mapped outputs provide a decision-support framework for regional restoration planning, while the tool itself can be adapted to other geographies.

## Features
- Identifies potential restoration areas for mangroves, saltmarshes, and seagrasses
- Distinguishes between passive and active restoration opportunities
- Integrates multiple spatial criteria including wave exposure, shoreline substrate, and shoreline stability
- Considers land tenure in restoration site selection
- Provides outputs for different restoration scenarios

## Requirements
- ArcGIS Pro 3.0.1 or later
- Python 3.x (as included with ArcGIS Pro)

## Installation
1. Clone this repository to your local machine
2. Ensure you have ArcGIS Pro 3.0.1 or later installed
3. Open the tool in ArcGIS Pro

## Usage
1. Open the BCE Restoration Tool in ArcGIS Pro
2. Load your input data layers (see Data Requirements section)
3. Select the target BCE type for restoration (mangroves, saltmarshes, or seagrasses)
4. Choose whether to limit site selection to historically suitable areas
5. Select desired coastal geomorphic and hydrodynamic attributes
6. Specify suitable ranges or thresholds for each attribute
7. Run the tool
8. Review the output maps and tables

For more detailed instructions, please refer to the user manual in the `docs` folder.

## Data Requirements
The tool requires the following input data layers:
1. Current BCE distribution (high-resolution, e.g., 1-5 m)
2. Historic BCE distribution (if available)
3. Coastal erosion sensitivity
4. Shoreline substrate erodibility
5. Significant wave height
6. Land tenure

All layers should cover the coastline of interest and be in a compatible GIS format (e.g., shapefile, geodatabase feature class).

## Outputs
The tool generates the following outputs:
1. Map of potential restoration areas, symbolized by different attributes and BCE type
2. Table summarizing total restorable area by:
   - BCE type (mangroves, saltmarshes, seagrasses)
   - Suitability class
   - Land tenure category
3. Distance calculations from each potential restoration site to the nearest existing mangrove, saltmarsh, and seagrass habitats

These areas were further categorized into passive and active restoration opportunities across different scenarios.

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
