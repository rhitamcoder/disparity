# ⚖️ Disparity

**A data analysis of fatal police shootings in the US, examined alongside poverty, education, income, and racial demographics.**

Disparity is a Python and Jupyter Notebook project that explores fatal police shootings in the United States between **January 2015 and July 2017**, using data compiled by [The Washington Post](https://www.washingtonpost.com/graphics/investigations/police-shootings-database/). It combines the shooting records with US Census city-level data on poverty, high school completion, median income, and racial makeup to ask how these factors relate to where and to whom fatal force is applied.

> **A note on the data:** This is an educational analysis of a public dataset. The records represent real people, and the data has known limitations in collection and reporting. Findings show patterns in this specific dataset and time window, and should not be read as causal claims.

---

## 📊 What This Project Explores

- Poverty rate and high school graduation rate by US state, and whether the two move together
- The racial makeup of each US state
- Fatalities by race, gender, and age, including how age distributions differ across groups
- Manner of death by gender (box plots)
- Whether the people killed were armed, and with what
- The share of victims showing signs of mental illness
- The 10 cities with the most fatal shootings
- Rate of death by race in those top cities, compared against each city's demographics
- A choropleth map of fatalities by US state, compared against poverty levels
- Trends in the number of fatal shootings over time

---

## 🛠️ Tech Stack

- **Python 3**
- **pandas** and **numpy** for cleaning, merging, and analysis
- **matplotlib** and **seaborn** for statistical plots (joint plots, KDE, regression)
- **plotly** (`express` and `graph_objects`) for donut charts, box plots, and choropleth maps
- **Jupyter Notebook**

---

## 📁 Project Structure

```
disparity/
├── Fatal_Force_start.ipynb                   # Starter notebook (questions, no solutions)
├── Fatal_Force_solved.ipynb                  # Complete analysis with visualizations
├── Deaths_by_Police_US.csv                   # Fatal police shootings (2,535 records)
├── Median_Household_Income_2015.csv          # Median income by US city
├── Pct_Over_25_Completed_High_School.csv     # High school completion by city
├── Pct_People_Below_Poverty_Level.csv        # Poverty rate by city
├── Share_of_Race_By_City.csv                 # Racial demographics by city
└── README.md
```

---

## 📦 Datasets

| File | Key Columns | Description |
|------|-------------|-------------|
| `Deaths_by_Police_US.csv` | `name`, `date`, `manner_of_death`, `armed`, `age`, `gender`, `race`, `city`, `state`, `signs_of_mental_illness`, `threat_level`, `flee`, `body_camera` | One row per fatal shooting, Jan 2015 to Jul 2017 |
| `Median_Household_Income_2015.csv` | `Geographic Area`, `City`, `Median Income` | 2015 median household income by city |
| `Pct_Over_25_Completed_High_School.csv` | `Geographic Area`, `City`, `percent_completed_hs` | Share of adults over 25 with a high school diploma |
| `Pct_People_Below_Poverty_Level.csv` | `Geographic Area`, `City`, `poverty_rate` | Share of residents below the poverty line |
| `Share_of_Race_By_City.csv` | `Geographic area`, `City`, `share_white`, `share_black`, `share_native_american`, `share_asian`, `share_hispanic` | Racial composition by city |

---

## ▶️ Getting Started

### Prerequisites

```
pip install numpy pandas matplotlib seaborn plotly jupyter
```

### Running the Notebook

```
git clone https://github.com/rhitamcoder/disparity.git
```
```
cd disparity
```
```
jupyter notebook Fatal_Force__solved_.ipynb
```

To work through the analysis yourself, open `Fatal_Force_start.ipynb` instead. It contains the same questions without the solutions.

> **Tip:** Some CSV files use Windows-1252 encoding, so load them with `encoding="windows-1252"` in `pd.read_csv()` if you see character errors.

---

## 📚 Further Reading

For the full, continually updated dataset and reporting, see [The Washington Post's police shootings database](https://www.washingtonpost.com/graphics/investigations/police-shootings-database/).

---

## 📝 License

The code in this repository (notebooks and analysis) is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

> **Note:** The MIT License applies to the code only. The datasets are third-party and included for educational and analysis purposes; they are not covered by this repository's license. Please check the original sources for their terms if you intend to reuse the data.

## 🙌 Acknowledgements

Police shooting data compiled by [The Washington Post](https://www.washingtonpost.com/graphics/investigations/police-shootings-database/). City-level demographic, income, education, and poverty data from US Census sources.
