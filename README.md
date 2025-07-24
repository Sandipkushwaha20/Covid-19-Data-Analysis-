# Covid-19 Data Analysis & Visualization

## Project Overview
This project presents a comprehensive Exploratory Data Analysis (EDA) of Covid-19 and Vaccination datasets for India, spanning two years. The primary objective is to extract actionable insights about the pandemic's progression, its impact across Indian states, and the effectiveness and reach of the vaccination drive. The project leverages Python for data analysis and visualization, and Tableau for advanced visual storytelling.

## Significance
Understanding the spread and control of Covid-19 is crucial for public health planning, resource allocation, and policy-making. This project:
- Reveals trends in infection, recovery, and mortality rates across states.
- Highlights disparities in vaccination coverage.
- Provides gender-based and state-wise vaccination insights.
- Offers visual tools for stakeholders to interpret the pandemic's evolution and the vaccination campaign's success.

## Datasets
1. **Covid-19 Case Data (`covid_19_india.csv`)**
   - Columns: `Sno`, `Date`, `Time`, `State/UnionTerritory`, `ConfirmedIndianNational`, `ConfirmedForeignNational`, `Cured`, `Deaths`, `Confirmed`
   - Daily records of Covid-19 cases, recoveries, and deaths for each state/UT.

2. **Vaccination Data (`covid_vaccine_statewise.csv`)**
   - Columns include: `Updated On`, `State`, `Total Doses Administered`, `First Dose Administered`, `Second Dose Administered`, `Male (Doses Administered)`, `Female (Doses Administered)`, `Covaxin (Doses Administered)`, `CoviShield (Doses Administered)`, `Total Individuals Vaccinated`, and more.
   - Daily vaccination statistics, including gender and age group breakdowns, for each state/UT.

## Workflow
### 1. Data Import & Initial Exploration
- Load datasets into Pandas DataFrames.
- Inspect structure, dimensions, and column names.
- Preview data samples to understand content and quality.

### 2. Data Cleaning & Preprocessing
- Drop irrelevant columns (e.g., `Sno`, `Time`, nationality-specific columns).
- Convert date columns to datetime objects for time-series analysis.
- Handle missing/null values to ensure data integrity.
- Standardize column names for consistency.
- Engineer new features (e.g., calculate `Active_Cases` as `Confirmed - (Cured + Deaths)`).

### 3. Data Aggregation & Transformation
- Create pivot tables to summarize confirmed, cured, and death counts by state.
- Calculate recovery and mortality rates for each state.
- Sort and rank states by key metrics (confirmed cases, deaths, active cases).
- Aggregate vaccination data by state, gender, and age group.

### 4. Visualization & Analysis
- **Bar Plots:**
  - Top 10 states with most active cases.
  - Top 10 states with highest deaths.
  - Top 5 most and least vaccinated states.
- **Line Plots:**
  - Trends of confirmed, cured, and death cases over time for top affected states.
- **Pie Charts:**
  - Gender-wise vaccination distribution (Male vs Female).
- **Heatmaps & Styled Tables:**
  - Visualize state-wise recovery and mortality rates.
- **Tableau Dashboards:**
  - Interactive global and India-specific Covid-19 visualizations (external to this repo).

### 5. Insights & Interpretation
- Identify states with highest/lowest infection and vaccination rates.
- Analyze gender disparities in vaccination.
- Track the effectiveness of the vaccination drive over time.
- Provide actionable recommendations based on findings.

## Tech Stack
- **Python Libraries:**
  - Pandas (data manipulation)
  - Matplotlib, Seaborn (static visualizations)
  - Plotly (interactive visualizations)
- **Tools:**
  - Google Colab (notebook environment)
  - Tableau (advanced dashboards)

## How to Use
1. **Clone the Repository**
   ```bash
   git clone <repo-url>
   ```
2. **Open the Notebook**
   - Launch `covid_data_analysis_project.ipynb` in Google Colab or Jupyter Notebook.
3. **Upload Datasets**
   - Ensure `covid_19_india.csv` and `covid_vaccine_statewise.csv` are available in the notebook's working directory or update the file paths accordingly.
4. **Run Cells Sequentially**
   - Execute each cell to perform data loading, cleaning, analysis, and visualization.
5. **Explore Visualizations**
   - Review the generated plots and tables for insights.
   - For Tableau dashboards, refer to the Tableau Public link (if provided).

## Project Structure
```
├── covid_19_india.csv                # Covid-19 case data (India)
├── covid_vaccine_statewise.csv       # Vaccination data (India)
├── covid_data_analysis_project.ipynb # Main analysis notebook
├── README.md                         # Project documentation
```

## Key Insights (Sample)
- Maharashtra, Kerala, and Delhi reported the highest number of cases and deaths.
- States like Uttar Pradesh and Rajasthan led in vaccination numbers, while some northeastern states lagged behind.
- Male and female vaccination rates were nearly balanced, with minor disparities in some states.
- Recovery rates improved significantly post-vaccination rollout.

## Limitations
- Data is limited to the provided time frame and may not reflect the most recent trends.
- Some columns in the datasets may have missing or inconsistent values.
- Tableau dashboards are not included in this repository but can be shared upon request.

## Conclusion
This project demonstrates the power of data analysis and visualization in understanding and combating a global health crisis. The insights derived can inform public health strategies, highlight areas needing attention, and celebrate successes in the fight against Covid-19.

---
*For questions, suggestions, or access to Tableau dashboards, please contact the project maintainer.*


