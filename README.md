
---

# **Charlotte Neighborhoods Geospatial Analysis for Optimal Location Selection**

## **Overview**

This project focuses on leveraging geospatial data and clustering techniques to optimize the selection of office or warehouse locations within Charlotte, North Carolina. By analyzing the geographic distribution of neighborhoods and exploring nearby venues using the Foursquare API, the project identifies optimal locations based on accessibility, amenities, and other factors critical for operational efficiency.

## **Table of Contents**
1. [Project Objective](#project-objective)
2. [Data Collection](#data-collection)
3. [Data Cleaning and Preparation](#data-cleaning-and-preparation)
4. [Geospatial Mapping](#geospatial-mapping)
5. [Venue Exploration with Foursquare API](#venue-exploration-with-foursquare-api)
6. [Clustering Analysis](#clustering-analysis)
7. [Visualization and Results](#visualization-and-results)
8. [Challenges and Solutions](#challenges-and-solutions)
9. [Future Work](#future-work)
10. [Installation](#installation)
11. [Usage](#usage)
12. [Contributing](#contributing)
13. [License](#license)

## **Project Objective**
The primary goal of this project is to optimize the selection of office or warehouse locations in Charlotte, NC, by:
- Mapping the geographic distribution of neighborhoods.
- Exploring nearby venues and amenities using the Foursquare API.
- Clustering neighborhoods to identify the most suitable locations based on accessibility, amenities, and operational efficiency.

## **Data Collection**
The project gathers data from the following sources:
- **Zip Code Data**: Retrieved from the "Zip Codes to Go" website, which provides essential zip code, city, and county information for North Carolina.
- **Geographical Coordinates**: Additional latitude and longitude data obtained from the `uszips.csv` dataset.

## **Data Cleaning and Preparation**
- **Location Filtering**: The data is filtered to focus on relevant zip codes, cities, and counties within Charlotte, NC.
- **Dataset Merging**: The zip code data is merged with geographical coordinates to ensure each neighborhood is accurately represented by its latitude and longitude.
- **Data Refinement**: Irrelevant or incorrect zip codes are removed to focus solely on the neighborhoods pertinent to the analysis.

## **Geospatial Mapping**
- **Geocoding for Charlotte**: The central coordinates of Charlotte are determined using the Nominatim geocoding service from the `geopy` library, providing a base for visualizing the city’s neighborhoods.
- **Interactive Map Creation**: An interactive map is generated using the `folium` library, allowing users to visualize the distribution of neighborhoods across Charlotte.

## **Venue Exploration with Foursquare API**
- **API Integration**: The project utilizes the Foursquare API to explore and analyze venues around specific neighborhoods.
- **Retrieving and Structuring Venue Data**: Venue data, including names, categories, and locations, is retrieved and organized into a DataFrame for further analysis. This information is critical in assessing the accessibility and amenities of potential office or warehouse locations.

## **Clustering Analysis**
- **Clustering for Optimal Locations**: The `KMeans` algorithm is employed to cluster neighborhoods based on their geographical attributes and the availability of nearby venues. This clustering helps in identifying regions within Charlotte that offer the most favorable conditions for business operations.
- **Determining Optimal Clusters**: Techniques like the elbow method may be used to determine the number of clusters, ensuring that the identified locations are truly optimal for the intended purpose.
- **Visualization of Clusters**: The clustered neighborhoods are visualized on the interactive map, highlighting areas that are ideal for office or warehouse setup.

## **Visualization and Results**
- **Final Map and Clusters**: The project culminates in an interactive map showcasing Charlotte’s neighborhoods, with each cluster color-coded to indicate the most suitable locations for office or warehouse placement.
- **Cluster Analysis**: Detailed analysis of each cluster reveals key characteristics, such as proximity to essential services, transportation hubs, and other amenities, which are crucial for operational success.

## **Challenges and Solutions**
- **Data Limitations**: Limited availability of pre-existing neighborhood data necessitated manual data creation from maps, emphasizing the importance of data accuracy.
- **API Rate Management**: Effective handling of Foursquare API rate limits was crucial to maintaining the flow of data retrieval and analysis.

## **Future Work**
- **Enhanced Clustering Techniques**: Future efforts could include more sophisticated clustering techniques and the integration of additional data sources.
- **Application to Other Cities**: The methodology could be expanded to analyze and optimize location selection in other cities, providing a versatile tool for urban planning and business strategy.

## **Installation**
To run this project locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Shreyash-Gaur/Geospatial_Analysis.git
   cd Geospatial_Analysis
   ```

2. **Install Required Packages**:
   Ensure you have Python installed & Install the required packages.

3. **Set Up Foursquare API**:
   Obtain your Foursquare API credentials:
   ```bash
   CLIENT_ID=your_foursquare_client_id
   CLIENT_SECRET=your_foursquare_client_secret
   ```

4. **Run the Analysis**:
   Run the Jupyter notebook or script to perform the analysis:
   ```bash
   jupyter notebook analysis.ipynb
   ```

## **Usage**
- **Interactive Map**: Use the interactive map to explore Charlotte’s neighborhoods and assess the suitability of different regions for office or warehouse locations.
- **Venue Analysis**: Leverage the Foursquare API integration to explore nearby amenities, crucial for making informed location decisions.
- **Cluster Insights**: Analyze the clusters to identify the most strategically beneficial locations for business operations.

## **Contributing**
Contributions are welcome! Please fork the repository and create a pull request with your improvements or new features.

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.

---