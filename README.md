# NASA Exoplanets: SQL and Python Data Analysis

An exploratory data analysis of more than 5,000 exoplanets from the NASA Exoplanet Archive, built for the CS 260 Database and Data Visualization final project at DeSales University.

**Team:** Sebastian Ombati and Tommy Williams

**Notebook:** [nasa_exoplanets_analysis.ipynb](nasa_exoplanets_analysis.ipynb)

## Tools

Python, SQL (SQLite), pandas, NumPy, Matplotlib, Google Colab

## Data

- **Main dataset:** [NASA Exoplanets on Kaggle](https://www.kaggle.com/datasets/adityamishraml/nasaexoplanets), sourced from the NASA Exoplanet Archive. 5,250 planets and 13 variables, including distance, host star brightness, planet type, discovery year, mass, radius, orbital radius, orbital period, eccentricity, and detection method.
- **Second dataset:** a confirmed exoplanets table with each planet's discovery facility and orbital eccentricity, joined to the main table on planet name.

## What we did

- Loaded the CSV data into a SQLite database and documented a schema for it
- Profiled every variable with SQL (distinct values, min, max, average, missing values)
- Used SQL aggregation, filtering, and joins to answer analysis questions
- Removed outliers before correlation analysis
- Built bar charts, line charts, histograms, and scatter plots with Matplotlib

## Key findings

- **Discovery spikes:** Exoplanet discoveries jumped in 2014 and 2016, driven by the processing of Kepler Space Telescope data. 2016 alone had over 1,400 transit discoveries.
- **Kepler leads:** Kepler produced over 2,000 confirmed transit discoveries, far more than any other facility, with its follow-up K2 mission in second place.
- **Earth-like distance does not mean Earth-like planet:** Only a small number of planets orbit between 0.7 and 1.5 AU from their star, and most of them are gas giants.
- **Mostly circular orbits:** About 80% of exoplanets have an eccentricity between 0 and 0.1.
- **Distance and brightness:** Host star distance and apparent magnitude have a moderate positive correlation (r = 0.64), so farther stars tend to look dimmer.
- **Oblong orbits:** La Silla Observatory stood out for discovering high-eccentricity planets, which raises questions for future research.

## Contributions

| Section | Contributor |
|---|---|
| 3.1 Just-right orbit planets by type | Sebastian Ombati |
| 3.2 to 3.5 Transit trends, eccentricity, brightness vs. distance, discoveries over time | Tommy Williams |

## Running the notebook

Open the notebook in Google Colab. The main dataset loads automatically from GitHub. Sections that use the second dataset expect a file named `confirmed_exoplanets.csv` to be uploaded to the Colab session first.
