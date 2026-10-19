
# Automated Nuclear Detection, Measurement, and Isolation Using QuPath

## Overview

This project provides a Groovy script for QuPath 0.7 designed to automate nuclear detection, quantitative measurement, and isolation in histology and cytology images. The workflow facilitates the extraction of individual nuclei for morphological analysis and subsequent quantitative studies.

The script uses QuPath's watershed-based cell detection algorithm and allows configurable parameters for nuclear detection, size filtering, background subtraction, and image processing.

## Features

- **Automated nuclear detection:** Identifies nuclei using hematoxylin optical density in brightfield images or a selected channel in fluorescence images.
- **Nuclear filtering:** Excludes detections touching image borders and applies configurable circularity criteria.
- **Nuclear isolation:** Exports individual nuclei as TIFF images, with the area outside each nuclear contour replaced by a white background.
- **Labeled mask generation:** Creates a labeled image identifying detected nuclear objects.
- **Quantitative measurements:** Exports nuclear measurements to CSV files for further statistical analysis.
- **Configurable parameters:** Allows adjustment of nuclear area, detection threshold, smoothing, background subtraction, and padding.
- **Batch-compatible workflow:** Can be adapted for processing multiple images within a QuPath project.

## Output Files

For each processed image, the script generates:

- Individual nuclear images in TIFF format.
- A TIFF image containing the isolated nuclear regions against a white background.
- A PNG version of the combined nuclear image.
- A labeled nuclear mask in TIFF format.
- A CSV file containing nuclear measurements.

## Requirements

- QuPath 0.7
- Images compatible with QuPath
- Appropriate pixel calibration for reliable measurements in physical units

## Configuration

The script includes parameters that can be adjusted according to the image type and analysis requirements, including:

- Image type: brightfield or fluorescence.
- Nuclear detection threshold.
- Minimum and maximum nuclear area.
- Background subtraction radius.
- Gaussian smoothing.
- Border exclusion.
- Nuclear masking and padding.

**Important:** The provided configuration sets the pixel size to 0.26 µm/pixel. Verify the calibration settings before processing images, particularly when working with datasets acquired at different magnifications or resolutions.

## Applications

This workflow can support quantitative morphological studies of nuclei in histological and cytological specimens. The exported images and measurements can be used for downstream statistical analysis, group comparisons, and research workflows.

The script is intended as a research tool. Detection parameters and segmentation results should be evaluated for each dataset, and automated measurements should be validated before drawing diagnostic or scientific conclusions.

## License

Add the license appropriate for your project if you intend to distribute or reuse this code publicly.
