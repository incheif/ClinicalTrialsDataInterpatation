# Clinical Trials Data Interpretation

## Overview

This project is designed to process and interpret clinical trial data stored in nested JSON format. By utilizing Python's `pandas` library, the project converts raw JSON data into a structured DataFrame with proper labeling, making it easier to analyze and visualize the data. The code also includes an optimized method for classifying countries into various regions, ensuring efficient data processing even with large datasets.

## Features

- **Nested JSON Flattening**: Transforms complex nested JSON structures into flat, tabular data.
- **Region Classification**: Classifies countries into predefined regions using an optimized, vectorized approach.
- **Efficient Data Processing**: Combines multiple clinical trial records into a single DataFrame for easier analysis.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/clinical-trials-data-interpretation.git
    cd clinical-trials-data-interpretation
    ```

2. **Install the required packages**:
    Make sure you have Python installed. Then, install the necessary packages using pip:
    ```bash
    pip install pandas
    ```

## Usage

1. **Load the JSON Data**:
   Ensure your clinical trial data is stored in a `data.json` file in the root directory.

2. **Run the Script**:
   Execute the Python script to process the data.
    ```bash
    python process_clinical_trials.py
    ```

3. **Output**:
   The processed data will be available as a Pandas DataFrame, which you can then export to a CSV file or analyze further within the script.

## Code Explanation

### 1. Flattening Nested JSON Data
The `flatten` function recursively processes the nested JSON structure, converting it into a flat dictionary. This is essential for transforming the data into a tabular format suitable for analysis.

### 2. Creating DataFrames
Each clinical trial's data is flattened and converted into a Pandas DataFrame. All individual DataFrames are then combined into a single DataFrame using `pd.concat()`.

### 3. Optimized Region Classification
Countries are classified into regions using a vectorized approach, avoiding inefficient nested loops. This ensures that the code runs efficiently even with large datasets.

## Example

Here is a snippet of how the code works:

```python
import json
import pandas as pd

# Load the JSON data from the file
with open('data.json', 'r', encoding='utf-8') as file:
    data = json.load(file)

# List to store individual ClinicalTest DataFrames
ClinicalTest_dfs = []

# Flattening function and DataFrame creation...
```

## Contributing

Contributions are welcome! If you have any improvements, please feel free to fork the repository and create a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

