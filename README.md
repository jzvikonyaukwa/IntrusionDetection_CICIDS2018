# IntrusionDetection_CICIDS2018


# CICIDS2018 Data Cleaning and Preprocessing

This project involves loading, cleaning, and preprocessing a large dataset from the CICIDS2018 intrusion detection dataset. The steps involved in this project are outlined below:

### Project Overview

- **Loading Data**: The project begins with iterating through a directory to collect all CSV file paths and then reading them into a list of DataFrames.
- **Concatenating DataFrames**: All the DataFrames are concatenated into a single large DataFrame for ease of processing.
- **Column Cleanup**: Column names are stripped of whitespace to ensure uniformity.
- **Handling Mixed Data Types**: During the initial load, columns with mixed data types were identified. These were handled by specifying the appropriate data types where necessary.
- **Removing Duplicates**: Exact duplicate rows were identified and removed from the dataset to ensure data integrity.
- **Handling Infinity Values**: Infinity values in certain columns were identified and handled using K-Nearest Neighbors (KNN) imputation to replace them with more realistic values.
- **Data Type Conversion**: Several columns were converted from object types to numeric types to enable better analysis.
- **Date Parsing**: Timestamps were converted to `datetime` objects for proper temporal analysis.
- **Label Encoding**: The target variable, representing different types of attacks, was simplified and encoded into a numeric format for model compatibility.
- **Correlation Analysis**: A correlation matrix was computed to identify relationships between different features in the dataset.

### Key Functions and Techniques Used

- **Pandas**: For data manipulation and analysis.
- **NumPy**: For handling numerical operations.
- **KNN Imputer**: For filling in missing or infinity values with more realistic data points based on the nearest neighbors.
- **Label Encoding**: For transforming categorical labels into numerical values that can be fed into machine learning models.

### Dataset Overview

- **Total Rows**: 8,284,254
- **Total Columns**: 80
- **Main Labels**: The dataset includes labels such as `Benign`, `DDoS`, `DoS`, `Bot`, `Infiltration`, `Brute Force`, and `SQL Injection`.
- **Preprocessing Outcome**: After cleaning and preprocessing, the dataset was reduced to 7,853,981 rows with all features cleaned and ready for model building.

### Next Steps

- **Modeling**: The cleaned dataset is now ready for machine learning model development, focusing on intrusion detection.

### Acknowledgments

- **CICIDS2018 Dataset**: The dataset was sourced from the Canadian Institute for Cybersecurity (CIC), which provides open datasets for cybersecurity research.

