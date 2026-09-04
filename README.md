# Smart Waste Collection Prediction

A machine learning project that explores smart-bin sensor data to predict whether waste bins require emptying and support data-driven waste collection planning.

## Project Overview

Waste collection can become inefficient when collection schedules do not reflect how quickly individual bins fill. Some bins may be collected before necessary, while others may require collection earlier than scheduled.

This project explores how data science and machine learning can support smarter waste collection by analyzing smart-bin data and predicting whether a bin requires emptying.

The project combines data analysis, machine learning, clustering, and geospatial visualization to demonstrate a data-driven approach to waste collection planning.

## Business Problem

Traditional fixed waste collection schedules may not accurately reflect the condition of individual waste bins.

A predictive system could help waste management teams identify bins that require collection and prioritize resources more effectively.

The main question addressed by this project is:

> **Can smart-bin characteristics and sensor measurements be used to predict whether a waste bin requires emptying?**

## Project Objectives

The project aims to:

- Explore and clean smart-bin data.
- Identify characteristics associated with bin-emptying requirements.
- Develop a machine learning model for predicting whether a bin requires emptying.
- Evaluate the model using appropriate classification metrics.
- Identify bins that may require collection priority.
- Explore geographic grouping of bins to support collection planning.
- Visualize collection information using an interactive map.

## Dataset

The primary dataset contains **4,638 observations and 10 variables** describing smart-bin measurements and characteristics.

The variables include:

- `Class` – bin emptying status and target variable.
- `FL_A`, `FL_B` – numerical sensor measurements.
- `FL_A_3`, `FL_B_3` – additional sensor measurements.
- `FL_A_12`, `FL_B_12` – additional sensor measurements.
- `VS` – numerical sensor measurement.
- `Container Type` – type of waste container.
- `Recyclable fraction` – category describing the recyclable characteristics of the waste.

The target variable contains two classes:

- `Emptying`
- `Non Emptying`

Initial inspection showed that the two classes are approximately balanced.

## Project Workflow

The project follows the following workflow:

1. **Business Understanding**
2. **Data Understanding**
3. **Data Preparation**
4. **Exploratory Data Analysis**
5. **Machine Learning**
6. **Model Evaluation**
7. **Collection Prioritization**
8. **Geographic Visualization**
9. **Conclusions and Recommendations**

## Repository Structure

smart-waste-collection-prediction/
│
├── data/
│   ├── raw/
│   │   ├── Smart_Bin.csv
│   │   └── waste-management-status-in-major-towns-of-kenya.csv
│   │
│   └── processed/
│       └── smart_bin_cleaned.csv       # created later
│
├── notebooks/
│   └── smart_waste_collection_prediction.ipynb
│
├── outputs/
│   └── Smart_Waste_Collection_Routes.html
│
├── README.md
├── requirements.txt
└── .gitignore


## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Folium
- Jupyter Notebook

## Preliminary Findings

Initial data inspection identified several important characteristics:

- The target variable is approximately balanced between `Emptying` and `Non Emptying`.
- A small number of missing values are present in several numerical variables.
- The original dataset contains duplicate observations that require removal before modelling.
- Preliminary analysis suggests that variables such as `FL_B`, `FL_B_3`, `FL_B_12`, and `VS` differ between the two target classes and may contain useful predictive information.

Further exploratory analysis and machine learning will be used to investigate these relationships.

## Geographic Visualization

The project includes an interactive geographic visualization to demonstrate how predicted collection priorities could be represented spatially.

> **Note:** The geographic coordinates used in the mapping component are synthetically generated within approximate Nairobi boundaries for demonstration purposes. They do not represent actual waste-bin locations.

## Model Results

Model development and evaluation are currently in progress.

This section will be updated with the final model, evaluation metrics, and key findings after the modelling stage is completed.

## Limitations

- The geographic coordinates used for visualization are synthetic rather than actual bin locations.
- The project currently demonstrates collection prioritization and geographic grouping rather than full vehicle route optimization.
- Further validation would be required before applying the model to real-world waste collection operations.

## Future Improvements

Potential extensions include:

- Using real GPS coordinates for waste-bin locations.
- Incorporating time-based waste generation patterns.
- Comparing multiple classification algorithms.
- Adding model hyperparameter tuning.
- Developing actual vehicle route optimization.
- Deploying the model through an interactive application or dashboard.


## Author

**Kevin Ngunjiri**