# Qingdao-WCNA-Enteromorpha-Monitor
A cloud-based interactive GIS platform for monitoring Green Tide (Enteromorpha prolifera) in Qingdao WCNA using Google Earth Engine.
🌊 Qingdao WCNA Enteromorpha Monitoring System

This project is a cloud-based interactive monitoring platform developed using Google Earth Engine (GEE), specifically designed to identify and analyze the outbreaks of Enteromorpha prolifera (green tide) in the coastal waters of the Qingdao West Coast New Area (WCNA).

📌 Project Overview

Every summer, the outbreak of green tides poses a significant challenge to the marine ecosystem and coastal economy of the Yellow Sea. Leveraging the powerful computational capabilities of Google Cloud and integrated Sentinel-2 Surface Reflectance products, this project establishes a comprehensive Web-GIS ecosystem that combines real-time monitoring, automated alerting, AI-driven decision support, and data sharing.

🌟 Key Features

1. Interactive Temporal-Spatial Monitoring

Annual Temporal Switching: Supports dynamic loading of high-resolution imagery spanning from 2019 to 2025.

Dynamic Layer Control: Users can adjust layer opacity and customize theme colors (e.g., Warning Red, Cyber Green) for tailored visualization.

2. Scientific Detection Algorithm

NDVI Differencing: Utilizes the Normalized Difference Vegetation Index to precisely extract floating algae.

B4 Band Threshold Filtering: Implements a B4 < 1200 logic to effectively eliminate spectral interference from high-turbidity suspended sediment in near-shore waters.

3. Multi-dimensional Visualization Modalities

Binary Classification Maps: Clearly defines the spatial distribution and boundaries of the algae blooms.

Intensity Heatmaps: Represents algae density (NDVI abundance) through smooth color gradients.

4. Micro-scale Point Inspection (Point Inspector)

Time-series Trend Retrieval: By clicking any point on the map, the system instantaneously generates an NDVI evolution chart for that specific coordinate between June and July.

5. Smart Decision Support & Export

Administrative Alerting: Automatically triggers "High-Risk" or "Routine Monitoring" management recommendations based on detected coverage area.

One-click Data Export: Facilitates immediate downloading of CSV statistical reports and high-resolution GeoTIFF raster maps.

Multi-model AI Integration: Connects with frontier AI engines like DeepSeek and Gemini to provide semantic-level analytical support.

📸 App Preview

screenshot-main.png

🛠️ Technical Architecture

Data Sources

Primary: COPERNICUS/S2_SR_HARMONIZED (Sentinel-2 MSI)

Secondary: JRC/GSW1_4/GlobalSurfaceWater (Water Masking)

Boundary: Custom Vector Assets (users/Qiyuan_Zheng/myshapes)

Core Algorithms

Index: $NDVI = (B8 - B4) / (B8 + B4)$

Filter: $B4_{threshold} < 1200$ (Sediment suppression)

Synthesis: Quality Mosaic (Based on maximum NDVI values)

🔗 Access URL

🚀 Launch:(https://my-project-287143.projects.earthengine.app/view/qingdao-enteromorpha-monitor)

(Please replace the link above with your actual published GEE App URL.)

📖 How to Use Source Code

Environment Setup: Register and log in to Google Earth Engine.

Copy Code: Open the GEE Code Editor.

Create Script: Copy the contents of code.js from this repository into the script area.

Configure Assets:

Ensure your asset manager contains the required study area vectors, or replace the path users/Qiyuan_Zheng/myshapes in the code with your own FeatureCollection.

Run: Click the Run button to initialize the interactive interface.


📧 Contact

Author: Qiyuan Zheng

Institution: [China University of Petroleum]

Email: [2382891455@qq.com]

GitHub: https://github.com/Zheng-qiyuan
