# Uber Rides Data Analysis

## Project Overview

This project is part of my Data Science portfolio and focuses on analyzing Uber ride data to uncover patterns in ride usage, temporal distributions, purposes, and mileage. The primary objective is to perform exploratory data analysis (EDA) to derive actionable insights and develop a baseline predictive model for ride distance (miles). This analysis aims to support operational decisions, such as optimizing driver allocation and understanding user behavior, which can benefit ride-sharing platforms.

The project includes data cleaning, feature engineering, EDA, and a simple linear regression model to predict ride miles. All steps are documented in a Jupyter Notebook, ensuring reproducibility and clarity for stakeholders, recruiters, or fellow data scientists.

## Dataset

The dataset used is UberDataset.csv, sourced from GeeksforGeeks. It contains 1156 records of Uber rides with the following key features:

* `START_DATE`, `END_DATE`: Timestamps for ride start and end.
* `CATEGORY`: Ride category (e.g., Business, Personal).
* `START`, `STOP`: Pickup and drop-off locations.
* `MILES`: Distance traveled (target variable for prediction).
* `PURPOSE`: Purpose of the ride (e.g., Meeting, Meal/Entertain).

> **Note:** The dataset is included in the repository for convenience. Alternatively, it can be downloaded from the source link above.

## Technologies and Dependencies

This project was developed using Python 3.10 in a Conda environment. The key libraries are specified in `environment.yml` for reproducibility.

* **Language:** Python 3.10
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Modeling:** Scikit-learn
* **Environment:** Conda

To install dependencies, use:
```
conda env create -f environment.yml
conda activate python-uber-data-analysis
```

## Project Structure

* `python-uber-data-analysis.ipynb`: Main Jupyter Notebook containing data loading, cleaning, feature engineering, EDA, modeling, and evaluation.
* `UberDataset.csv`: Dataset file for analysis.
* `environment.yml`: Conda environment specification for reproducibility.
* `.gitignore`: Ignores temporary files, caches, and Conda environment directories.
* `README.md`: This file, providing project overview and instructions.

## Setup Instructions

To run this project locally, follow these steps:

**1. Clone the repository:**
```
git clone https://github.com/arielpuifil/python-uber-data-analysis.git
cd python-uber-data-analysis
```

**2. Set up the Conda environment:**
```
conda env create -f environment.yml
conda activate python-uber-data-analysis
```

**3. Launch Jupyter Notebook:**
```
jupyter notebook python-uber-data-analysis.ipynb
```

**4. Ensure the dataset:**

* The UberDataset.csv file is included in the repository. If not found, download it from GeeksforGeeks and place it in the project root.

**5. Run the notebook:** 

* Execute all cells in python-uber-data-analysis.ipynb to reproduce the analysis and results.

## Key Results

The analysis revealed the following insights:

**Ride Patterns:** Most rides occur in the afternoon, with "Business" as the dominant category and "Meeting" as the primary purpose.

**Distance Trends:** Ride distances vary by time of day, with longer rides observed during certain hours.

**Predictive Model:** A linear regression model was trained to predict ride miles, achieving an RMSE of approximately 3.45 miles and an R² of 0.12, indicating a baseline fit with room for improvement.

> **Note:** Detailed EDA, including visualizations (e.g., histograms, count plots, scatter plots), and model evaluation (e.g., residual plots) are documented in `python-uber-data-analysis.ipynb`.

## Usage

**To explore the analysis:**

1. Open `python-uber-data-analysis.ipynb` in Jupyter Notebook.
2. Follow the structured sections: data loading, cleaning, feature engineering, EDA, modeling, and evaluation.
3. Review visualizations and insights to understand ride patterns and model performance.

**For stakeholders:**

* The insights can inform driver scheduling during peak hours.
* The predictive model serves as a baseline for forecasting ride distances, potentially aiding operational planning.

## Limitations and Future Work

**Limitations:**

* Small dataset size (1156 records) limits generalizability.
* High cardinality in location features (`START`, `STOP`) was excluded, reducing spatial insights.
* The linear regression model shows modest performance due to limited feature complexity.

**Future Work:**

* Incorporate geospatial analysis using coordinates or location embeddings.
* Experiment with advanced models (e.g., Random Forest, Gradient Boosting).
* Collect additional data for more robust insights.
* Address potential biases in ride purpose categorization.

## Ethical Considerations

* **Data Privacy:** The dataset is anonymized, but care should be taken to ensure no sensitive information (e.g., exact locations) is exposed in real-world applications.
* **Bias:** The dataset may overrepresent certain ride purposes or categories, potentially skewing insights. Validation with diverse data is recommended.

## References

**Dataset:** GeeksforGeeks. (n.d.). UberDataset.csv. Retrieved from https://media.geeksforgeeks.org/wp-content/uploads/20240919115958/UberDataset.csv

**Tutorial Inspiration:** GeeksforGeeks. (n.d.). Uber Rides Data Analysis using Python. Retrieved from https://www.geeksforgeeks.org/data-analysis/uber-rides-data-analysis-using-python/

**Libraries:** Pandas, Seaborn, Scikit-learn