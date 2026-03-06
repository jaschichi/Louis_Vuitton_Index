# Louis_Vuitton_Index
A data analytics project that builds a market potential index to identify optimal locations for luxury retail expansion using demographic and economic indicators.
# LV Index: Luxury Retail Market Potential Model

## Project Overview

The LV Index is a data-driven framework designed to identify potential locations for luxury retail expansion.

The model measures how similar a ZIP code is to existing Louis Vuitton store locations in the United States. By analyzing demographic and socioeconomic indicators, the LV Index helps identify neighborhoods that resemble proven luxury retail markets.

This approach provides a structured and repeatable way to support luxury store location decisions with data rather than intuition.

---

## Business Problem

Luxury brands carefully choose store locations because their success depends heavily on the surrounding market environment.

Successful luxury retail locations typically share several characteristics:

- Strong purchasing power
- High income and education levels
- Demographic profiles aligned with luxury consumption
- Exposure to premium retail environments

The key question this project answers is:

**Which ZIP codes most closely resemble existing Louis Vuitton store markets?**

---

## Methodology

### 1. Identify Existing LV Store Locations

We collected **112 Louis Vuitton store ZIP codes across the United States**.  
These locations represent proven luxury retail markets.

### 2. Build a Comparison Dataset

To evaluate potential markets, we gathered demographic profiles for other ZIP codes within the same cities as LV stores.  
This allows each neighborhood to be compared against existing LV environments.

### 3. Select Key Demographic Indicators

Key indicators used in the analysis include:

- Household income
- Education levels
- Population size
- Median age
- Diversity indicators
- Household and dependency structure

These variables describe the socioeconomic environment where luxury retail typically performs well.

### 4. Logistic Regression Modeling

A logistic regression model was used to determine which demographic factors are most associated with existing LV store locations.

Model structure:

- **Dependent variable**
  - 1 = ZIP code contains an LV store
  - 0 = ZIP code does not contain an LV store

- **Independent variables**
  - normalized demographic indicators

The model coefficients indicate how strongly each factor influences the likelihood of a ZIP code hosting an LV store.

### 5. Construct the LV Index

The LV Index measures similarity between a candidate ZIP code and the average LV store ZIP profile.

Steps:

1. Compute the average demographic profile of LV store ZIP codes.
2. Measure the difference between each candidate ZIP code and the LV benchmark.
3. Apply weights derived from the logistic regression coefficients.
4. Aggregate the weighted differences into a single score.

Interpretation:

- **Higher LV Index score → greater similarity to LV store markets**
- **Lower score → less alignment with luxury retail environments**

---

## Key Insights

Analysis reveals that LV store locations tend to share consistent demographic patterns, including:

- Higher household income levels
- Higher education attainment
- Specific age distributions
- Distinct diversity patterns

The LV Index also highlights several ZIP codes that strongly resemble LV markets even though they are not traditional luxury districts.

Examples include:

- Miami Beach, FL (33140)
- Towson, MD
- Sacramento, CA
- Tulsa, OK
- St. Paul, MN

These locations demonstrate how data can reveal expansion opportunities beyond obvious luxury corridors.

---

## Strategic Applications

The LV Index can support luxury retail strategy in several ways:

- Identify high-potential expansion markets nationwide
- Compare neighborhoods within the same city
- Bring objective data into store placement decisions
- Apply the same framework across multiple luxury brands

The methodology can be extended to brands such as:

- Chanel
- Hermès
- Dior
- Cartier

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Data Visualization Tools

---

## Conclusion

Luxury retail expansion should not rely solely on intuition.

The LV Index provides a **data-driven, scalable, and repeatable framework** for identifying markets that resemble today’s successful luxury store environments.

This approach allows luxury brands to better understand where future customers are likely to be and supports strategic retail expansion decisions for the years ahead.
