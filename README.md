# Suyana template

This repository provides a standardized framework for managing data science projects at Suyana, emphasizing consistency, scalability, and collaboration.

## Repository structure

```
suyana_template/
|-- data/
|   |-- raw/            # Raw datasets (e.g., satellite data)
|   |-- processed/      # Processed and cleaned datasets
|-- code/               # Python scripts or Jupyter notebooks
|-- docs/               # Reports, visualizations, and documentation
|-- README.md           # Repository overview
|-- requirements.txt    # Python dependencies
|-- .gitignore          # Files excluded from version control
```

The template organizes the workflow into the following directories:

- `data/raw/`: raw datasets, such as satellite imagery or weather observations.
- `data/processed/`: cleaned and transformed datasets ready for analysis.
- `code/`: R, python scripts or Jupyter notebooks for analysis, modeling, and visualization.
- `docs/`: reports, presentations, and other documentation materials.


## Example workflow

### Load raw data

```python
import pandas as pd

# Load raw dataset
raw_data = pd.read_csv('data/raw/climate_data.csv')
print(raw_data.info())
```

### Process and save data

```python
# Clean data
processed_data = raw_data.dropna(subset=['temperature', 'precipitation'])

# Save to processed folder
processed_data.to_csv('data/processed/cleaned_climate_data.csv', index=False)
print("Processed data saved.")
```

### Analyze data

```python
# Perform analysis
mean_temp = processed_data['temperature'].mean()
print(f"Average Temperature: {mean_temp:.2f}")
```

### Document results

Summarize findings and include any visualizations in the `docs/` directory.

## Authorship and contributions

The code in this repository was developed by the **Suyana team**, with individual contributions from team members. To ensure proper attribution, include your name and contact details in the readme, or script headers. For example:

```python
# Author: Daniela Belén Risaro
# Email: daniela@suyana.org
# Date: January 2025
# Description: Script for processing climate data and creating climatologies.
```

## Notes

Up to now this template is for internal use only.
