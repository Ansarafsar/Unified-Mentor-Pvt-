---

# Heart Disease Diagnostic Data Analysis

This repository contains the code and analysis for the heart disease diagnostic data. The goal of this project is to perform ETL (Extract, Transform, Load) and EDA (Exploratory Data Analysis) on the dataset to uncover meaningful insights and create visualizations.

## Dataset

The dataset can be downloaded from [this link](https://drive.google.com/file/d/1U8CHK_ye5jmcuYEeIOYIYcMzK2ooqLUV/view).

## Installation

To run this project, you need to have the following Python packages installed:

- pandas
- numpy
- matplotlib
- seaborn

You can install these packages using pip:

```bash
pip install pandas numpy matplotlib seaborn
```

## Usage

1. Clone this repository to your local machine.
2. Download the dataset and place it in the same directory as the notebook.
3. Run the Jupyter notebook `heart_disease_analysis.ipynb`.

## Project Structure

The project is structured as follows:

- **ETL Functions**: Extract, Transform, and Load data functions.
- **EDA Functions**: Perform exploratory data analysis.
- **Visualization Functions**: Create visualizations of the data.
- **Key Metrics and Relationships**: Find key metrics and relationships in the data.
- **Main Function**: Orchestrates the ETL and EDA processes.

## Functions

### ETL Functions

- `extract_data(file_path: str) -> pd.DataFrame`: Extracts the data from the given file path.
- `transform_data(df: pd.DataFrame) -> pd.DataFrame`: Transforms the data (handles missing values and data type conversions).
- `load_data(df: pd.DataFrame) -> pd.DataFrame`: Loads the transformed data (returns the transformed data).

### EDA Functions

- `perform_eda(df: pd.DataFrame)`: Performs exploratory data analysis (displays basic statistics and visualizes the data).

### Visualization Functions

- `create_visualizations(df: pd.DataFrame)`: Creates visualizations of the data (heart disease by gender and by age).

### Key Metrics and Relationships

- `find_key_metrics(df: pd.DataFrame)`: Finds key metrics and relationships in the data.

### Main Function

- `main(file_path: str)`: Orchestrates the ETL and EDA processes.

## Summary of Findings

- **Age Distribution**: The dataset shows the distribution of patients' ages.
- **Gender Distribution**: Visualization of heart disease cases by gender.
- **Age vs Cholesterol Levels**: Scatter plot showing the relationship between age and cholesterol levels.

## License

This project is licensed under the MIT License.

## Author

This analysis was conducted as part of a data science project. If you have any questions or suggestions, feel free to reach out!

---
