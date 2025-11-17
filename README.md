# 🌡️ European Cities Temperature Analysis - PCA Project

## 📋 Project Overview

This project applies **Principal Component Analysis (PCA)** to monthly temperature data from European cities to identify climate patterns based on geographical location. The analysis reveals how European cities cluster according to temperature characteristics and geographical factors.

## 🎯 Objective

To simplify the analysis of multidimensional temperature data and draw conclusions about European climate patterns using dimensionality reduction techniques.

## 📊 Dataset

**File:** `temperatures.csv`

**Variables:**
- **Monthly temperatures**: January through December
- **Additional variables**: 
  - Average temperature (`Moyenne`)
  - Thermal amplitude (`Amplitude`)
  - Geographical coordinates (`Latitude`, `Longitude`)
- **Cities**: Multiple European cities with their temperature profiles

## 🛠️ Methodology

### 1. Data Exploration & Preprocessing
- Correlation analysis between variables
- Data standardization (centering and scaling) for PCA
- Identification of strongly correlated variables

### 2. Principal Component Analysis
- **Components determined**: 2 principal components
- **Variance explained**: 
  - PC1: 78.0% 
  - PC2: 15.9%
  - **Total**: 93.9%

### 3. Component Selection Criteria
- **Kaiser's rule**: Eigenvalues > 1 (2 components)
- **Elbow method**: 3 components
- **Cumulative variance**: 2 components (93.9%)

## 🔍 Key Findings

### Interpretation of Principal Components

#### **PC1 (78.0%) - North-South Temperature Gradient**
- **Positive end**: Southern, warmer cities (Seville, Athens, Palermo)
- **Negative end**: Northern, colder cities (Reykjavik, St. Petersburg, Helsinki)
- **Key variables**: Average temperature, all monthly temperatures
- **Strong negative correlation**: Latitude

#### **PC2 (15.9%) - Continental vs Maritime Climate**
- **Positive end**: Continental cities (Kiev, Budapest, St. Petersburg)
- **Negative end**: Maritime cities (Dublin, Reykjavik, Edinburgh)
- **Key variables**: Thermal amplitude, summer months

### Climate Classification

European cities cluster into four main groups:

| Quadrant | Climate Type | Examples |
|----------|--------------|----------|
| **Q1** (Positive PC1, Positive PC2) | Warm + Continental | Athens, Budapest, Rome, Madrid |
| **Q2** (Negative PC1, Positive PC2) | Cold + Continental | Helsinki, Kiev, Moscow, Stockholm |
| **Q3** (Negative PC1, Negative PC2) | Cold + Maritime | Amsterdam, Berlin, Dublin, London |
| **Q4** (Positive PC1, Negative PC2) | Warm + Maritime | Lisbon, Paris, Barcelona, Bordeaux |

## 📈 Main Insights

1. **Dual Climate Classification**: European cities can be classified simultaneously by:
   - North-South axis (average temperature)
   - Continental-Maritime axis (thermal amplitude)

2. **Geographical Patterns**:
   - **Northwest**: Cold + Maritime
   - **Northeast**: Cold + Continental  
   - **Southwest**: Warm + Maritime
   - **Southeast**: Warm + Continental

3. **Climate Theory Confirmation**:
   - Oceanic influence softens temperatures (low amplitude)
   - Continentality extremizes temperatures (high amplitude)
   - Latitude is the dominant factor in average temperatures

4. **Notable Exceptions**:
   - Budapest and Milan appear as "Continental South"
   - Geneva appears as "Continental North" due to altitude

## 💻 Technical Implementation

### Dependencies
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
```
## Key Functions
  - Data standardization with StandardScaler
  - PCA implementation with sklearn.decomposition.PCA
  - Custom functions for elbow detection and contribution analysis
  - Correlation circle visualization
  - Quality of representation (COS²) calculation

## 📁 Project Structure
```
temperature_analysis_europe/
├── data/
│   └── temperatures.csv
├── docs/
│   └── temperature_analysis_europe.pdf
├── notebooks/
│   └── TP_PCA_template.ipynb
└── README.md
```

## 🚀 How to Run

1. Ensure all dependencies are installed
2. Place the temperatures.csv file in the data/ directory
3. Execute the analysis notebook or script
4. Review the generated visualizations and interpretations

📝 Conclusion
This PCA analysis successfully reduced 16-dimensional temperature data into 2 interpretable components that capture 93.9% of the variance. The results provide a clear framework for understanding European climate patterns and demonstrate the power of PCA for geographical and climatological data analysis.

The methodology can be extended to other geographical regions or additional climate variables for more comprehensive analysis.

Project completed as part of Unsupervised Learning coursework

## 🔗 [View Project on GitHub Pages](https://jmalfaro2019.github.io/temperature-PCA/)

📄  Full Report
📋  [Download PDF Report](docs/temperature_analysis_europe.pdf)

👨‍💻 Author
Jose Alfaro - [GitHub](https://github.com/jmalfaro2019) - [LinkedIn](https://www.linkedin.com/in/jose-alfaro-334327291)

### ⭐ Did you like this project? Give the repository a star!

