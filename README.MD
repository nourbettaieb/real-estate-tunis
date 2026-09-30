# Real Estate Tunisia — Data Analytics Project

![Status](https://img.shields.io/badge/Status-EDA%20Complete-green)
![Python](https://img.shields.io/badge/Python-3.13-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green)
![SQL](https://img.shields.io/badge/SQL-SQLite-orange)

## 📊 Project Overview

A complete **data analytics pipeline** for exploring a synthetic Tunisian real-estate dataset.

The project covers the full workflow from **data generation and cleaning to SQL storage, exploratory analysis, feature engineering, and data visualization**.

The main objective is to demonstrate how real-estate data can be transformed into structured insights about **prices, property characteristics, market segments, listing duration, and value-based screening**.

> **Important:** This project uses synthetic data generated with Python. It is inspired by Tunisian locations and real-estate characteristics but does not represent actual property transactions or the Tunisian real-estate market.

---

## 🎯 Project Objectives

* Generate a synthetic real-estate dataset inspired by Tunisia
* Clean and validate the data
* Perform feature engineering
* Store and query the data using SQL
* Perform exploratory data analysis (EDA)
* Analyze property prices and price per m²
* Compare property types and market segments
* Analyze listing duration and property characteristics
* Develop a value score for exploratory screening
* Identify properties matching predefined screening criteria
* Create visualizations to communicate key findings
* Prepare the dataset for a future Power BI dashboard

---

## 📁 Project Structure

```text
real-estate-tunis/
│
├── notebooks/
│   ├── 01_data_generation.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_sql_database.ipynb
│   └── 04_exploratory_analysis.ipynb
│
├── data/
│   ├── cleaned_properties.csv
│   ├── real_estate.db
│   ├── eda_investment_opportunities.csv
│   ├── eda_top_expensive.csv
│   ├── eda_best_price_m2.csv
│   └── eda_top_value_score.csv
│
├── sql/
│   ├── schema.sql
│   └── queries.sql
│
├── docs/
│   └── charts and project documentation
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 🛠️ Tech Stack

| Tool                 | Purpose                                 |
| -------------------- | --------------------------------------- |
| **Python**           | Data generation, cleaning and analysis  |
| **Pandas**           | Data manipulation and transformation    |
| **NumPy**            | Numerical operations                    |
| **Matplotlib**       | Data visualization                      |
| **Jupyter Notebook** | Interactive analysis and documentation  |
| **SQLite / SQL**     | Database storage and analytical queries |
| **Git & GitHub**     | Version control and project sharing     |
| **Power BI**         | Planned interactive dashboard           |

---

## 📊 Dataset Overview

The final cleaned dataset contains:

* **170 property listings**
* **20 variables**
* 5 property types:

  * Apartments
  * Villas
  * Duplexes
  * Houses
  * Land
* Multiple Tunisian-inspired locations and districts
* Property characteristics such as:

  * Price
  * Area
  * Bedrooms
  * Property type
  * Condition
  * Parking
  * Garden
  * Listing duration

### Main Variables

| Variable         | Description                                 |
| ---------------- | ------------------------------------------- |
| `price`          | Property price in TND                       |
| `price_per_m2`   | Price per square meter                      |
| `area`           | Property area in m²                         |
| `location`       | Property location                           |
| `district`       | District                                    |
| `property_type`  | Apartment, Villa, Duplex, House or Land     |
| `bedrooms`       | Number of bedrooms                          |
| `condition`      | Property condition                          |
| `has_parking`    | Whether parking is available                |
| `has_garden`     | Whether a garden is available               |
| `days_listed`    | Number of days the property has been listed |
| `price_category` | Budget to Ultra-Luxury segmentation         |
| `quality_score`  | Constructed quality indicator               |
| `features_score` | Parking/garden feature score                |
| `value_score`    | Constructed value-screening score           |
| `market_type`    | Urban, Coastal or Rural                     |

---

## 🔄 Data Pipeline

```text
Synthetic Data Generation
          ↓
Data Cleaning
          ↓
Feature Engineering
          ↓
SQLite Database
          ↓
SQL Analysis
          ↓
Exploratory Data Analysis
          ↓
Value-Based Screening
          ↓
Visualizations
          ↓
Power BI Dashboard (planned)
```

---

## 📓 Notebook Guide

### `01_data_generation.ipynb`

Generates the initial synthetic real-estate dataset.

The notebook creates property listings with variables such as:

* Property type
* Location
* Area
* Bedrooms
* Price
* Condition
* Parking
* Garden
* Listing dates

**Output:** Raw property dataset

---

### `02_data_cleaning.ipynb`

Prepares the generated data for analysis.

Main tasks include:

* Data quality checks
* Handling missing values
* Removing duplicates
* Data type correction
* Feature engineering
* Price per m² calculation
* Price category creation
* Market type classification
* Value score calculation

**Output:** `data/cleaned_properties.csv`

---

### `03_sql_database.ipynb`

Loads the cleaned dataset into a SQLite database.

The notebook demonstrates:

* Database creation
* Table creation
* Data loading
* SQL queries
* Analytical aggregations

**Database:** `data/real_estate.db`

---

### `04_exploratory_analysis.ipynb`

Performs the main exploratory data analysis.

The analysis covers:

* Market overview
* Property type analysis
* District analysis
* Price distributions
* Price per m²
* Area vs. price
* Bedrooms
* Property condition
* Parking and garden
* Price categories
* Market types
* Listing duration
* Value score
* Correlation analysis
* Property rankings
* Value-based screening

---

## 📈 Key Findings

The final dataset contains **170 listings**.

### Market Overview

* **Median price:** 182,574 TND
* **Median price per m²:** 1,301.49 TND/m²
* **Median area:** 140 m²
* **Median listing duration:** 16.5 days
* **Most common property type:** Apartment — 98 listings
* **Most common market type:** Rural — 87 listings

### Price & Area

Property area has a **0.65 positive correlation with total price**, indicating that larger properties generally tend to have higher prices within the dataset.

### Value Score

**43 properties (25.3%)** have a value score of at least 75.

The score is a constructed metric used for exploratory screening and should not be interpreted as an independent measure of real-world investment potential.

### Market Segmentation

Within this synthetic dataset:

* Urban properties have the highest average price and price per m².
* Coastal properties follow.
* Rural properties have lower average prices and price per m².

These patterns describe the generated dataset and should not be generalized to the Tunisian real-estate market.

---

## 🔎 Value-Based Screening

The project includes an exploratory screening process using predefined criteria:

* `value_score >= 75`
* `days_listed <= 30`
* Exclude land
* Price at or below the dataset median

The resulting properties are presented as **candidates for further investigation**, rather than actual investment recommendations.

The screening results are exported to:

```text
data/eda_investment_opportunities.csv
```

---

## 📊 Visualizations

The project includes visualizations covering:

* Property type distribution
* Average price by property type
* Average price by district
* Average price per m² by district
* Price distribution
* Price per m² distribution
* Area vs. price
* Average price by bedrooms
* Parking and garden analysis
* Price category analysis
* Market type analysis
* Listing duration
* Value score distribution
* Correlation matrix
* Top 10 most expensive properties
* Lowest price per m² properties
* Highest value-score properties

Charts are stored in the `docs/` directory.

---

## ⚠️ Dataset Limitations

This project uses a **synthetic real-estate dataset generated with Python**.

The dataset is inspired by Tunisian locations and common real-estate attributes, but it is not based on actual property transactions or a statistically representative sample of the Tunisian real-estate market.

The values for prices, areas, property types, conditions, and listing durations were generated programmatically. Some relationships between variables are therefore simplified and may not reflect real-world market behavior.

In particular:

* Some variables were generated independently.
* Certain relationships are based on simplified rules.
* The `value_score` is a constructed metric.
* The `condition` variable was randomly generated and should not be interpreted as causing differences in property prices.
* Correlations should not be interpreted as evidence of causation.

Therefore, the findings should be interpreted as **exploratory insights into the generated dataset**, rather than conclusions about the Tunisian real-estate market.

---

## 🚀 Getting Started

### Prerequisites

* Python 3.8+
* pip
* Jupyter Notebook or VS Code

### Installation

Clone the repository:

```bash
git clone https://github.com/nourbettaieb/real-estate-tunis.git

cd real-estate-tunis
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Open the project in Jupyter or VS Code and run the notebooks in order:

```text
01_data_generation
02_data_cleaning
03_sql_database
04_exploratory_analysis
```

---

## 💡 Skills Demonstrated

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Data Cleaning**
* **Feature Engineering**
* **Exploratory Data Analysis**
* **Statistical Analysis**
* **Data Visualization**
* **SQL / SQLite**
* **Database Design**
* **Git & GitHub**
* **Jupyter Notebooks**
* **Data Storytelling**

---

## 🔮 Future Improvements

Potential next steps include:

* Building an interactive **Power BI dashboard**
* Adding more real-world data sources
* Improving the value-scoring methodology
* Adding more advanced statistical analysis
* Exploring predictive price modelling
* Comparing multiple time periods if historical data becomes available

---

## 📄 License

MIT License — free to use and modify.

---

## 📧 Contact

**GitHub:** [@nourbettaieb](https://github.com/nourbettaieb)

**Email:** [nourbettaieb2@gmail.com](mailto:nourbettaieb2@gmail.com)

---

**Last Updated:** September 2026

**Project Status:** 🟢 EDA Complete — Power BI dashboard planned
