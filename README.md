# Indian States Mobility Analysis

This project focuses on classifying Indian states based on terrain-related features into three mobility categories — **Easy**, **Moderate**, and **Difficult** — using classical machine learning techniques such as **Random Forest**.

[Kaggle Link](https://www.kaggle.com/code/medhavitripathi/indian-states-mobility-analysis)

[Link to Dataset](https://www.kaggle.com/datasets/nehaprabhavalkar/india-gis-data)

The data used includes official shapefiles containing state boundaries and attributes.

- **Dataset Includes**:  
  - Shapefiles for Indian states  
  - National boundary shapefile for India  

- **Features Used**:  
  - Area of each state (in sq. km)  
  - Perimeter length (in km)  
  - Compactness ratio (area/perimeter²)  

- **Target Classes**:  
  - `Easy` — Highly traversable regions  
  - `Moderate` — Partially challenging terrain  
  - `Difficult` — Hard to navigate due to area/perimeter characteristics  

---

## Project Structure

- **Geospatial Data Handling**:
  - Loaded shapefiles using `GeoPandas`
  - Converted CRS for accurate area and distance calculations
  - Extracted geometrical features from polygons

- **Feature Engineering**:
  - Calculated `area_km2` and `perimeter_km` for each state
  - Derived `compactness = area / perimeter²` to assess terrain complexity
  - Manually assigned `mobility_class` labels based on feature thresholds

- **Data Visualization**:
  - Choropleth maps displaying terrain mobility classes across India
  - Seaborn plots for feature comparison
  - Distribution of states by mobility category

- **Model Training**:
  - Applied **Random Forest Classifier** for multi-class classification
  - Train-test split with stratification
  - Evaluation using accuracy, classification report, and confusion matrix

- **Final Output**:
  - Downloadable CSV file containing state-wise terrain mobility class
  - Interactive map with clear legend and boundary overlays

---

## Technologies and Tools

- **Languages**: Python  
- **Libraries**: GeoPandas, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
- **Platform**: Kaggle
