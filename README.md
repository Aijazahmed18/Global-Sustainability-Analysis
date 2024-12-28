# Global Emissions Analysis and Prediction

## Overview

This project analyzes a global dataset containing various environmental and socioeconomic indicators to explore relationships between factors like energy consumption, renewable energy adoption, GDP, and CO2 emissions. It uses data visualization and machine learning to provide insights into global trends and predict CO2 emissions based on these factors.

## Project Goals

*   **Data Exploration:** To visually explore patterns and trends in global environmental data.
*   **Relationship Analysis:** To understand the relationships between energy use, renewable adoption, economic factors, and carbon emissions.
*   **CO2 Emission Prediction:** To develop a machine learning model that can predict CO2 emissions based on selected features.
*   **Visualization of Key Findings:** To present the insights through interactive plots and charts.

## Dataset

The project uses the `global.csv` dataset, which includes various global indicators:
*   Socioeconomic factors like GDP per capita
*   Energy consumption data (fossil fuels, renewables)
*   Environmental metrics like CO2 emissions, and land area.

The original dataset can be found [here](link to the source of your dataset if available or remove if not).

## Libraries Used

*   **pandas:** For data manipulation and analysis.
*   **seaborn:** For creating statistical graphs and visualizations.
*   **matplotlib.pyplot:** For creating basic plots.
*   **plotly.express:** For creating interactive plots and visualizations.
*   **scikit-learn:** For machine learning tasks (data splitting, preprocessing, and model building).
*   **joblib:** For saving and loading machine learning models.

## Setup

### Prerequisites

*   Python 3.6+
*   Required Python packages (see below)

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [repository url]
    cd [repository name]
    ```
2.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```
    (You can create a `requirements.txt` file listing your dependencies using `pip freeze > requirements.txt`)

### Running the Code

*   Ensure that the `global.csv` file is placed in the root directory or provide the correct path when running the script.
*   Run the main script:
    ```bash
    python [your_script_name.py]
    ```

## Code Explanation

### Data Loading and Cleaning
*   The script loads the `global.csv` file using pandas and performs basic cleaning steps:
    *   Drops columns with high missing values.
    *   Fills remaining missing values using the mean of the respective column.
    *   Converts data types as necessary.
    *   Renames columns for readability.

### Exploratory Data Analysis (EDA)
*   The project generates interactive visualizations using `plotly` and `seaborn` to explore the data. These visualizations include:
    *   **Bubble Chart:** Visualizing the relationship between Access to Electricity and Renewable Energy share.
    *   **Animated Scatter Plot:** Showing changes over time in Fossil Fuel Use vs CO2 emissions, where bubble size indicates `Primary energy consumption per capita`.
    *  **Bubble Chart:** Visualizing the relationship between Energy Intensity and GDP per capita.

### Key Statistics
*   Prints the top 5 countries by:
    *   CO2 Emissions.
    *   Renewable Energy Share.
    *   GDP per Capita.
    *  Energy Intensity.

### Modeling
*   The project uses a Random Forest Regressor to predict CO2 Emissions.
*   The data is preprocessed using `StandardScaler` before training.
*   A train/test split of 80/20 is used to evaluate the model.
*   The model's performance is assessed using the R-squared score.
*   Feature Importance visualization is provided to assess each feature's importance to the prediction.
*    An "Actual vs Predicted" scatterplot shows the performance of the model.

### Model Saving
*   Saves the trained Random Forest model and the `StandardScaler` object using joblib.

## Output
The project will generate several PNG images of graphs and will save the machine learning model for future use:

### PNG Images:
*   `electricity_vs_renewable.png`: Bubble chart of Electricity access vs Renewable energy share.
*   `fossil_vs_co2_animated.png`: Animated scatter plot of fossil fuel use vs. CO2 emissions over time.
*   `energy_intensity_vs_gdp.png`: Bubble chart of Energy intensity vs GDP per capita.
*   `feature_importance.png`: Bar chart of feature importance in the model
*   `actual_vs_predicted.png`: Scatter plot comparing actual vs. predicted values of CO2 emissions.

### Model Files:
*   `rf_model.pkl`: Saved Random Forest model.
*   `scaler.pkl`: Saved StandardScaler object.

## Results
The project's visualizations provide insights into the relationships between the different environmental and socio-economic indicators, and the R-squared value of the model indicates its predictive performance.

## Future Improvements
*   Experiment with more machine learning models.
*   Include more feature engineering.
*   Add statistical tests to support the relationships seen in visualizations.
*   Include more advanced visualizations.

## Author

Aijaz Ahmed Chandio
