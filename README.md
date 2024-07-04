# Geospatial-Analysis-for-Outlier-Detection-in-Election-Data
This repo contains a project aimed at ensuring election integrity by detecting outlier polling units using geospatial analysis . It identifies polling units with voting results that significantly deviate from their neighboring units, which could indicate potential irregularities.  

Geospatial Analysis for Outlier Detection in Election Data
This project aims to ensure election integrity by identifying potential voting irregularities through geospatial analysis. By detecting outlier polling units where voting results deviate significantly from their neighbors, we can pinpoint areas that may warrant further investigation.

Data Preparation
Dataset
Source: Independent National Electoral Commission (INEC), ABIA STATE.
Format: CSV
Steps
Loading the Dataset: The dataset is loaded into a pandas DataFrame.
Geocoding: Longitude and latitude values for each polling unit are obtained using geocoding techniques.
Saving the Dataset: The updated dataset is saved with added longitude and latitude columns.
Methodology
Neighbor Identification
Neighbors are identified based on geographical proximity. A radius of 1 km is used to determine neighboring polling units.

Outlier Score Calculation
For each polling unit, the votes each party received are compared with those of its neighboring units. An outlier score is calculated based on the deviation of votes from neighboring units.

Sorting and Reporting
The dataset is sorted by the outlier scores for each party to identify the most significant outliers. A detailed report is generated explaining the methodology and findings.

Results
The results include:

Cleaned Dataset: A CSV file with added longitude and latitude values for each polling unit or ward, including calculated outlier scores for each party.
Sorted List: An Excel sheet showing a sorted list of polling units by outlier scores for each party.
Outlier Detection Report: A detailed report containing the methodology, summary of findings, top 3 outliers, and visualizations.
Conclusion
The analysis successfully identified outlier polling units, highlighting areas with potential voting irregularities. This methodology can be applied to ensure election transparency and integrity.

Usage
To run the analysis:

Clone the Repository:

git clone https://github.com/Bethel13/Geospatial-Election-Analysis.git
cd Geospatial-Election-Analysis
Install Dependencies:

pip install -r requirements.txt

Run the Analysis:
python geospatial_analysis.py

Dependencies
pandas
geopy
numpy
matplotlib
seaborn


