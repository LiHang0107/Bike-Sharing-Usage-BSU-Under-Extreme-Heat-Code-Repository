
# 🚲 Bike-Sharing Usage (BSU) Under Extreme Heat – Code Repository

This repository contains the code and data used for analyzing the impact of urban thermal environments and other environmental factors on bike-sharing usage (BSU) under extreme heat conditions. The analysis leverages **XGBoost** and **SHAP** to explore nonlinear relationships and interaction effects.

---

## 📁 **Project Structure**
```plaintext
├── data_processing.ipynb                       # Code for cleaning and processing raw data
├── interaction_plot.ipynb                      # Code for generating interaction effect plots using SHAP
├── variable_processing.ipynb                   # Code for constructing and processing feature variables
├── variables description and model selection.ipynb   # Description of variables and model selection criteria
├── XAI_modeling.ipynb                          # XGBoost modeling and SHAP analysis
├── data/                                       
│   ├── shp_data                                # Shapefile data for geographic analysis
│   ├── panel                                   # Cleaned panel data for modeling
│   ├── XAI_output                              # Model outputs from SHAP analysis
│   ├── raster_data                             # NDVI and other raster-based environmental data
│   ├── processed_bsu                           # Cleaned and aggregated BSU data
│   ├── weather                                 # Weather data used for modeling
│   └── combined_output300                      # Combined output data for validation and additional analysis
├── .ipynb_checkpoints                          # Notebook checkpoints for backup and autosave
├── requirements.txt                            # List of required Python packages
```

---

## 🚀 **Setup and Installation**
1. Clone this repository:
```bash
git clone https://github.com/LiHang0107/Bike-Sharing-Usage-BSU-Under-Extreme-Heat-Code-Repository
```

2. Install dependencies:
```bash
pip install -r requirements.txt  
```

---

## 🛠️ **Usage**
### 1. **Data Processing**
- Run `data_processing.ipynb` to clean and preprocess raw data.
- The processed data will be saved in `/data/processed_bsu/`.

### 2. **Variable Construction**
- Use `variable_processing.ipynb` to create and refine feature variables, including:
  - **POI Entropy Calculation** – Measures diversity of points of interest.
  - **Bus Distance Calculation** – Calculates the proximity of bike-sharing stations to bus stops.
  - **NDVI** – Measures the presence of greenery and vegetation cover.
- The outputs will be saved in `/data/variables/`.

### 3. **Model Selection and Description**
- `variables description and model selection.ipynb` provides detailed information on selected variables and justifies model choices.

### 4. **Modeling and SHAP Analysis**
- Run `XAI_modeling.ipynb` to train the XGBoost model and generate SHAP values.
- Outputs from SHAP analysis will be saved in `/data/XAI_output/`.

### 5. **Interaction Effects**
- Execute `interaction_plot.ipynb` to visualize the interaction between thermal and environmental factors.
- The interaction plot will show how different environmental factors influence BSU under varying heat conditions.

### 6. **Panel Data**
- Cleaned panel data for different time periods and weather conditions are stored in `/data/panel/`.
- This data includes weekday and weekend data for peak and non-peak hours.

---

## 📊 **Key Outputs**
- SHAP-based feature importance analysis  
- Nonlinear relationships between environmental factors and BSU  
- Interaction plots to explore combined effects of thermal and environmental factors  
- Geographic clustering results for region-based strategy analysis  

---

## 📜 **Data and Privacy**
- The raw data used in this study contains sensitive information and **cannot be shared** publicly.  
- Processed and anonymized data can be shared upon request for academic purposes.  

---

## 🌍 **Geographic and Environmental Data**
- **Shapefiles** for geographic analysis are stored in `/data/shp_data/`.
   - `fishnet_300` – Spatial grids for environmental matching.
   - `2021.03` – POI and urban infrastructure data from March 2021.
- **Raster Data** stored in `/data/raster_data/` includes NDVI and other environmental data used to evaluate green space and urban heat.

---

## 💡 **Policy and Analysis Insights**
This project investigates the impact of urban heat on bike-sharing from multiple perspectives:  
✅ **Temporal and spatial heterogeneity** – The relationship between Tmrt and BSU changes across different times and locations.  
✅ **Interaction effects** – High Tmrt weakens the positive impact of POI diversity and public transport proximity on BSU.  
✅ **Geographic variation** – Differences in cycling behavior between central and fringe areas suggest the need for targeted infrastructure and cooling strategies.  

---

## 🤝 **Contributing**
If you'd like to contribute to this project, please submit a pull request or contact me directly.

---

## 🏆 **Acknowledgements**
This work was supported by [Your Institution/Funding Body].

---

## 🔧 **Requirements**
The required Python packages are listed in `requirements.txt`. Install them using:
```bash
pip install -r requirements.txt
```

---

## ✅ **Extracted Requirements:**
Following are the extracted dependencies:
```plaintext
matplotlib
numpy
pandas
shap
sklearn
xgboost
```
