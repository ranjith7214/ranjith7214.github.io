---
title: "Overview"
permalink: /thermal-image/overview/
---
<!-- <div>
    <a href="https://github.com/AnshShah3009/AutonomousDrone" target="_blank" style="display: inline-block; padding: 10px 15px; background-color: #24292e; color: #ffffff; border-radius: 5px; font-family: Arial, sans-serif; text-decoration: none;">
        <i class="fab fa-github" style="margin-right: 5px;"></i> View on GitHub
    </a>
</div> -->

# Project Overview

## YouTube Video

<!--<iframe width="560" height="315" src="https://www.youtube.com/embed/QwA_yBjVZdA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->

![Image Description](/images/portfolio/AutonomousDrone/IMG_20191116_210726.jpg)

 
# Project: Thermal Image Conversion from RJPEG to TIFF for Photogrammetry and Orthophoto

## Objective:
Create a tool that converts thermal images from RJPEG to TIFF, specifically optimized for applications in photogrammetry and orthophoto generation, using the DJI thermal SDK and Python.

## Problem Statement:
Thermal images in the RJPEG format are widely used in aerial surveying and inspection, but they are not supported by many standard image processing software platforms. This limitation affects industries that rely on photogrammetry and orthophoto generation, such as agriculture, construction, and environmental monitoring.

## Solution:
Developed a Python-based tool utilizing the DJI thermal SDK to convert RJPEG thermal images into the more universally accepted TIFF format. This solution ensures compatibility with photogrammetry software, facilitating accurate and efficient generation of orthophotos and 3D models.

## Business Impact:

- **Increased Versatility**: By providing TIFF-compatible thermal images, the company can cater to clients in industries that rely on photogrammetry and orthophoto analysis.
- **Expanded Market Reach**: The tool opens up new opportunities by offering solutions for aerial surveyors and drone operators who need thermal imaging integrated with their standard workflows.
- **Enhanced Service Offering**: Packaging the tool with the DJI SDK dependency allows easy distribution, enabling clients to use it out of the box, further improving customer satisfaction.

## Steps:

1. **DJI SDK Integration**: Incorporated the DJI thermal SDK to accurately extract and process thermal data from RJPEG images.
2. **Image Parsing and Conversion**: Processed the thermal data and converted it to TIFF format for photogrammetry and orthophoto compatibility.
3. **Packaging**: Packaged the tool with the necessary DJI SDK components, ensuring that the tool can be easily installed and used by clients.
4. **Output**: Delivered high-quality TIFF files ready for use in photogrammetry software.

## Tools Used:

- DJI Thermal SDK
- Python
- Image libraries: OpenCV, Pillow

## Outcome:
This packaged solution allows companies to integrate thermal imaging data into their photogrammetry workflows, enabling more precise orthophoto generation. The inclusion of the DJI SDK ensures seamless operation, expanding the reach of thermal imaging services in surveying and aerial monitoring industries.
