# COVID-19 Citywise Map Visualization Project

## Overview
This project visualizes COVID-19 data across various Indian cities, mapping the state-wise confirmed cases and deaths using the Folium library. The data is sourced from two main sources: a JSON file (`capital_data.json`) containing geographical information of state capitals, and a live API providing COVID-19 statistics.

The visualization helps in understanding the COVID-19 impact across different regions by placing markers on the map according to the severity of deaths, using different colors to represent the scale of fatalities.

## Project Flow
1. **Data Collection**: 
   - COVID-19 data is fetched using the `requests` library from an external API (`https://api.covid19india.org/data.json`).
   - City and state geographical information is loaded from the `capital_data.json` file.

2. **Data Integration**: 
   - The script matches the state codes from the COVID-19 dataset and city dataset to merge relevant COVID-19 data (confirmed cases and deaths) with geographical coordinates.

3. **Map Visualization**:
   - Using the `folium` library, a map is created centered on India, with markers for each state capital.
   - Markers are colored based on the severity of COVID-19 deaths:
     - **Dark Red**: More than 50 deaths
     - **Red**: Between 20 and 50 deaths
     - **Orange**: Between 1 and 20 deaths
     - **Green**: 0 deaths
   - Markers also display a tooltip with details on confirmed cases and deaths.

4. **Output**: 
   - The generated map is saved as an HTML file (`map.html`) and automatically opened in Firefox.

