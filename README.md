# NHANES Diabetes Risk Analysis: Interactive Health Data Exploration

**SIT220 Data Wrangling - Final Project**  
**Student:** Vu Hoang Nam Doan  
**Student ID:** s224021565  
**Deakin University**

## Project Overview

This comprehensive data analysis project explores diabetes risk factors using the National Health and Nutrition Examination Survey (NHANES) 2021-2023 data. The project demonstrates advanced data wrangling techniques, interactive visualizations, and machine learning applications to identify key health patterns and socioeconomic disparities in diabetes prevalence.

## Research Objectives

- **Primary Goal**: Identify key predictors of diabetes risk in the US population
- **Secondary Goals**:
  - Analyze socioeconomic health disparities
  - Explore demographic patterns in health outcomes
  - Create interactive visualizations for health data exploration
  - Apply clustering techniques to identify health profiles
  - Implement dimensionality reduction for pattern recognition

## Dataset Information

The analysis utilizes 7 NHANES 2021-2023 datasets:

| Dataset | Description | Key Variables |
|---------|-------------|---------------|
| `DEMO_L` | Demographics | Age, Gender, Race, Income, Education |
| `BMX_L` | Body Measurements | BMI, Weight, Height |
| `GHB_L` | Glycohemoglobin | HbA1c levels, Diabetes indicators |
| `PAQ_L` | Physical Activity | Exercise patterns, Sedentary behavior |
| `INQ_L` | Income | Poverty index, Food security |
| `DIQ_L` | Diabetes | Diabetes diagnosis, Family history |
| `DR1TOT_L` | Dietary | Nutritional intake, Caloric consumption |

## Technical Implementation

### Data Wrangling Pipeline
- **Data Integration**: Merged 7 datasets using SEQN (sequence number)
- **Missing Data Handling**: KNN imputation for continuous variables
- **Feature Engineering**: Created composite health indicators
- **Data Validation**: Comprehensive quality checks and outlier detection

### Machine Learning Models
- **Random Forest Classification**: AUC = 0.737
  - Top predictors: Age (importance: 0.15), BMI (importance: 0.14)
- **K-means Clustering**: 4 distinct health clusters identified
- **Principal Component Analysis**: 47.60% variance explained by first two components

### Interactive Visualizations
- **Bokeh Library**: Interactive scatter plots, histograms, and heatmaps
- **Exploratory Data Analysis**: Multi-dimensional health data exploration
- **Dashboard Components**: Real-time filtering and selection capabilities

## Key Findings

### Primary Risk Factors
1. **Age**: Strongest predictor of diabetes risk
2. **BMI**: Critical body composition indicator
3. **Socioeconomic Status**: Significant health disparities identified
4. **Physical Activity**: Protective effect against diabetes

### Health Clusters
Four distinct population segments identified:
- **Cluster 1**: Low-risk, young adults
- **Cluster 2**: Moderate-risk, middle-aged
- **Cluster 3**: High-risk, elderly with comorbidities
- **Cluster 4**: Mixed-risk, socioeconomically disadvantaged

### Socioeconomic Insights
- Lower income associated with higher diabetes prevalence
- Educational attainment correlates with better health outcomes
- Food security impacts nutritional choices and health

## Getting Started

### Prerequisites
```bash
# Python 3.8+
# Jupyter Notebook or JupyterLab
# Quarto (for document generation)
```

### Required Libraries
```python
pandas>=1.5.0
numpy>=1.24.0
scikit-learn>=1.2.0
bokeh>=3.0.0
seaborn>=0.12.0
matplotlib>=3.6.0
xarray>=2023.1.0
```

### Installation
```bash
# Clone or download the project
cd task1.7hd

# Install required packages
pip install pandas numpy scikit-learn bokeh seaborn matplotlib xarray

# For Quarto rendering (optional)
quarto install
```

## Project Structure

```
task1.7hd/
├── README.md               # This file
├── report.ipynb            # Main Jupyter notebook
├── report.qmd              # Quarto document version
├── report.py               # Python script version
├── BMX_L.XPT               # Body measurements data
├── DEMO_L.XPT              # Demographics data
├── DIQ_L.XPT               # Diabetes data
├── DR1TOT_L.XPT            # Dietary data
├── GHB_L.XPT               # Glycohemoglobin data
├── INQ_L.XPT               # Income data
└── PAQ_L.XPT               # Physical activity data
```

## Usage

### Option 1: Jupyter Notebook
```bash
# Launch Jupyter
jupyter lab

# Open report.ipynb
# Run all cells to reproduce analysis
```

### Option 2: Quarto Document
```bash
# Render HTML report
quarto render report.qmd --to html

# Render PDF report
quarto render report.qmd --to pdf

# Render HTML report
quarto render report.qmd --to html

# Render PDF report
quarto render report.qmd --to pdf

# Render both formats
quarto render report.qmd
```

### Option 3: Python Script
```bash
# Run complete analysis
python report.py
```

## Output Files

After running the analysis, you'll generate:
- **HTML Report**: Interactive web-based report with embedded visualizations
- **PDF Report**: Print-ready academic document
- **Interactive Plots**: Bokeh HTML files for exploration
- **Model Results**: Classification metrics and cluster assignments

## Academic Context

This project fulfills the requirements for **SIT220 Data Wrangling** at Deakin University, demonstrating:

- **Data Integration**: Complex multi-source data merging
- **Data Cleaning**: Advanced missing data techniques
- **Exploratory Analysis**: Interactive visualization development
- **Statistical Modeling**: Machine learning implementation
- **Reporting**: Professional documentation and presentation

## Performance Metrics

| Model | Metric | Value |
|-------|--------|-------|
| Random Forest | AUC | 0.737 |
| Random Forest | Accuracy | ~73% |
| K-means | Clusters | 4 |
| PCA | Variance Explained | 47.60% |
| Data Completeness | After Imputation | >95% |

## Methodology Highlights

### Data Wrangling Techniques
- Multi-dataset joins using common identifiers
- KNN imputation for missing continuous variables
- Categorical encoding for machine learning
- Outlier detection and treatment
- Feature scaling and normalization

### Statistical Analysis
- Correlation analysis for feature selection
- Principal Component Analysis for dimensionality reduction
- Clustering validation using silhouette scores
- Cross-validation for model performance

### Visualization Strategy
- Interactive Bokeh plots for data exploration
- Statistical plots for pattern identification
- Cluster visualization in reduced dimensions
- Demographic comparison charts

## Research Impact

This analysis contributes to understanding:
- **Public Health**: Diabetes risk factor identification
- **Health Equity**: Socioeconomic health disparities
- **Data Science**: Advanced wrangling techniques
- **Policy Implications**: Evidence-based health interventions

## Contributing

This is an academic project for SIT220 Data Wrangling. For questions or suggestions:
- **Student**: Vu Hoang Nam Doan
- **Student ID**: s224021565
- **Institution**: Deakin University

## License

This project is submitted for academic evaluation at Deakin University. Data sources are from CDC NHANES public datasets.

## References

- CDC NHANES 2021-2023 Data Documentation
- Scikit-learn Documentation
- Bokeh Interactive Visualization Library
- Quarto Scientific Publishing System

---

**Note**: This project demonstrates advanced data wrangling techniques as part of the SIT220 curriculum, showcasing real-world application of data science methods to public health research.