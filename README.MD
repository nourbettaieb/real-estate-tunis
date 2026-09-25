# Real Estate Tunisia - Data Analytics Project

![Status](https://img.shields.io/badge/Status-In%20Progress-blue)
![Python](https://img.shields.io/badge/Python-3.13-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green)

## 📊 Project Overview

A complete **data pipeline + analytics solution** for Tunisian real estate market analysis. 
From data generation → cleaning → SQL database → Power BI dashboards.

**Goal:** Identify investment opportunities, market trends, and price patterns across Tunisia.

---

## 🎯 Project Objectives

✅ Generate realistic Tunisian real estate data  
✅ Clean & engineer features for analysis  
✅ Store data in SQL database  
✅ Perform exploratory data analysis  
✅ Create interactive Power BI dashboards  
✅ Identify best investment opportunities  

---

## 📁 Project Structure
real-estate-tunis/
├── notebooks/
│ ├── 01_data_generation.ipynb # Generate 200 realistic properties
│ ├── 02_data_cleaning.ipynb # Data cleaning & feature engineering
│ ├── 03_sql_database.ipynb # Load data to SQL
│ └── 04_analysis.ipynb # EDA & insights
├── data/
│ ├── raw_properties.csv # Generated raw data
│ ├── cleaned_properties.csv # Cleaned data ready for analysis
│ └── data_dictionary.md # Column descriptions
├── sql/
│ ├── schema.sql # Database schema
│ └── queries.sql # Analysis queries
├── docs/
│ ├── methodology.md # How we built this
│ └── insights.md # Key findings
├── requirements.txt # Python dependencies
├── .gitignore
└── README.md 

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python 3.13** | Data generation, cleaning, analysis |
| **Pandas** | Data manipulation & transformation |
| **NumPy** | Numerical operations |
| **Jupyter** | Interactive notebooks |
| **SQL** | Database queries |
| **Power BI** | Interactive dashboards (coming soon) |

---

## 📊 Data Overview

**Sample Generated Data:**
- 200 realistic Tunisian properties
- Real districts & market prices
- Property types: Apartments, Villas, Land, Duplexes, Houses
- Realistic pricing by location & type
- Features: parking, garden, condition

**Data Points Tracked:**
- Price (TND)
- Area (m²)
- Location & District
- Property Type
- Bedrooms
- Condition
- Amenities (parking, garden)
- Days Listed
- Date Scraped

---

## 🚀 Getting Started

### Prerequisites
```bash
Python 3.8+
pip
Jupyter Notebook or VS Code
```

### Installation

1. **Clone repository**
```bash
git clone https://github.com/nourbettaieb/real-estate-tunis.git
cd real-estate-tunis
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Run notebooks**
```bash
jupyter notebook
```

Or open in VS Code and run cells.

---

## 📋 Notebook Guide

### `01_data_generation.ipynb`
Generates 200 realistic Tunisian property listings with:
- ✓ Price correlates with district
- ✓ Area matches property type
- ✓ Bedrooms correlate with size
- ✓ Realistic date distributions

**Output:** `data/raw_properties.csv`

### `02_data_cleaning.ipynb` 
Cleans data and creates features:
- ✓ Remove duplicates
- ✓ Handle missing values
- ✓ Create price categories
- ✓ Calculate price per m²
- ✓ Assign value scores
- ✓ Categorize market type

**Output:** `data/cleaned_properties.csv`

### `03_sql_database.ipynb` 
- Load cleaned data to SQL database
- Create tables & indexes
- Write analysis queries

### `04_analysis.ipynb` 
- Exploratory data analysis
- Find patterns & trends
- Identify best investments

---

## 📈 Key Findings (To Be Updated)

- Average property price: **~150,000 TND**
- Most common type: **Apartments (45%)**
- Most expensive district: **Tunis Centre**
- Best value district: **Kasserine**
- Recent listings: **50% listed in last 7 days**

---

## 💡 Features Engineered

| Feature | Purpose |
|---------|---------|
| `price_per_m2` | Compare properties fairly |
| `price_category` | Segment market (Budget→Ultra-Luxury) |
| `days_listed` | How long on market |
| `value_score` | Investment potential ranking |
| `features_score` | Parking + garden count |
| `quality_score` | Property condition ranking |
| `market_type` | Urban / Coastal / Rural |

---

## 📊 Dashboard 

Power BI dashboard will include:
- 📍 Market overview by district
- 💰 Price analysis & trends
- 🏠 Property type distribution
- 🎯 Investment opportunities
- 📈 Days-on-market analysis
- 🌟 Best value properties

---

## 🔍 Skills Demonstrated

✅ Data Generation (Realistic synthetic data)  
✅ Data Cleaning & Transformation  
✅ Feature Engineering  
✅ SQL Database Design  
✅ Exploratory Data Analysis (EDA)  
✅ Data Visualization (Power BI)  
✅ Python Programming (Pandas, NumPy)  
✅ Git & GitHub (Version control)  
✅ Jupyter Notebooks (Documentation)  

---



## 🤝 Contributing

This is a learning project, but feel free to suggest improvements!

---

## 📧 Contact

**GitHub:** [@nourbettaieb](https://github.com/nourbettaieb)  
**Available for:** Freelance data analytics projects  
**Email:** nourbettaieb2@gmail.com  

---

## 📄 License

MIT License - Free to use & modify

---

**Last Updated:** September 2026  
**Status:** 🟡 In Progress (Data generation & cleaning complete)