## Overview
This Python script performs a data analytics project that analyzes the difference in interest between the movies 'Barbie' and 'Oppenheimer' in various US states. The project aims to visualize this difference on a US map and determine which movie generated more interest across different regions.

## Prerequisites
Make sure you have the following installed before running the script:
- Python 3.x
- pandas library
- geopandas library
- matplotlib library

## Installation
1. Install Python from the official website: https://www.python.org/downloads/
2. Install required libraries using pip:
   ```
   pip install pandas geopandas matplotlib
   ```

## How to Use
1. Download the dataset file required for analysis from the provided link:
   - [Download 'geoMap.csv' data](https://trends.google.com/trends/explore?date=2023-07-15%202023-07-22&geo=US&q=Barbie,Oppenheimer&hl=en)

2. Place the downloaded CSV file in the `data` directory of your project folder and ensure the GeoJSON file is accessible.

3. Run the Python script in a terminal or an IDE that supports Python.

4. The script will process the data, calculate the percentage difference between interest in 'Barbie' and 'Oppenheimer' for each region, and then convert this difference to a range that attempts to recreate the range used in the news source.

5. The generated map will be saved as `US_BarbHeimer_Interest_Map.jpeg` in the current working directory.

## Code Explanation
- The script uses `pandas` to read the data from the CSV file and perform data manipulation.
- The function `get_percentage_difference` calculates the percentage difference between 'Barbie' and 'Oppenheimer' interest for each region.
- The script reads the US states' geometries from the provided GeoJSON file using `geopandas`.
- The percentage difference data is then merged with the US states data to associate each region with its corresponding difference value.
- The script converts the percentage difference to a range by multiplying it by 40 and rounding it.
- Finally, the script plots the US map using `matplotlib` and saves it as an image file.

## Notes
This script presents the findings based on the provided dataset. It appears that the 'Barbie' movie generated more interest than 'Oppenheimer' across all US states, contrary to what the news source reported.

Please note that this analysis is based on the available data, and for a comprehensive and accurate understanding, further investigations and data sources may be required.

For additional insights or improvements, you may consider expanding the dataset or exploring other factors that could influence interest in movies, such as promotional activities, release dates, or regional demographics.

**Disclaimer:** The accuracy and validity of the conclusions drawn from this analysis depend on the quality and representativeness of the data used. Always verify and cross-reference the results with multiple sources before making any critical decisions or drawing significant conclusions based on this analysis.
