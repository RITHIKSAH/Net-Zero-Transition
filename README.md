# UK Greenhouse Gas Emissions: Trend Analysis & 5-Year Forecast

### Data Analytics | Python | Time-Series Forecasting | Sustainability | Net-Zero Transition

## Project Overview

The United Kingdom has committed to achieving **net-zero greenhouse gas emissions by 2050**, making emissions monitoring, forecasting and sector-level analysis essential for understanding progress towards decarbonisation.

This project analyses **35 years of UK greenhouse gas emissions data (1990–2024)** and develops a five-year forecast for **2025–2029** using statistical time-series forecasting techniques.

Using publicly available data from the Office for National Statistics (ONS), the project explores historical emissions patterns, identifies high-emission sectors and evaluates potential future reductions.

The analysis demonstrates how Python-based data preparation, statistical modelling and visualisation can turn complex environmental datasets into actionable insights relevant to renewable energy, sustainability and net-zero planning.

## Project Objectives

The primary objectives are to:

1. Clean and transform historical UK greenhouse gas emissions data into structured, analysis-ready datasets.
2. Examine long-term national emissions trends between 1990 and 2024.
3. Develop and compare statistical forecasting models to estimate emissions from 2025 to 2029.
4. Identify sectors and industries contributing most significantly to UK greenhouse gas emissions.
5. Highlight the implications of emissions trends for decarbonisation strategies and the UK's net-zero ambitions.

## Technologies & Techniques

| Category | Technologies / Methods |
|---|---|
| Programming | Python |
| Development Environment | Jupyter Notebook |
| Data Processing | Pandas, Data Cleaning, Data Transformation |
| Statistical Modelling | Holt's Linear Trend Exponential Smoothing |
| Forecasting Techniques | Standard Holt Model, Damped Trend Model |
| Analytics | Time-Series Analysis, Sector-Level Analysis |
| Visualisation | Line Charts, Donut Charts, Bar Charts |
| Data Source | Office for National Statistics (ONS) |

## Dataset

**Source:** ONS Provisional Atmospheric Greenhouse Gas Emissions Dataset

**Historical coverage:** 1990–2024

**Measurement:** Thousand tonnes of CO₂ equivalent (CO₂e)

The dataset contains historical greenhouse gas emissions information across UK industry sections and industry groups.

### Data Preparation

The original ONS dataset required significant preprocessing before it could be used for statistical analysis.

The preparation workflow included:

- Identifying valid data headers across complex spreadsheet structures.
- Removing metadata, explanatory notes and unnecessary columns.
- Separating industry sections and industry groups into structured datasets.
- Handling non-numeric placeholders and converting numeric fields.
- Extracting annual national emissions observations.
- Creating reusable CSV datasets for analysis and forecasting.

**Data-quality consideration:** Some suppressed values represented by placeholders such as `[low]` were converted to zero during preprocessing. These values do not necessarily represent genuine zero emissions, and this treatment should be considered when interpreting sector-level results.

The resulting datasets supported consistent historical analysis, forecasting and visualisation.

## Forecasting Methodology

Two statistical forecasting approaches were applied to estimate future UK greenhouse gas emissions.

### 1. Holt's Linear Trend Model

Holt's Linear Trend Exponential Smoothing estimates future values using two components:

- **Level:** The estimated current magnitude of the emissions series.
- **Trend:** The estimated rate of change over time.

This approach was selected because the historical annual emissions data exhibits a long-term downward trend without an evident seasonal pattern.

### 2. Damped Trend Model

The Damped Trend variation extends Holt's method by progressively reducing the influence of the historical trend over the forecast horizon.

This helps avoid unrealistically aggressive long-term projections, particularly where unusual events have influenced historical observations.

The COVID-19 period (2020–2021) was considered carefully because the sharp reduction and subsequent recovery in emissions could affect trend estimation.

Both approaches were used to generate and compare five-year emissions forecasts.

## Key Findings & Results

### 1. UK Emissions Declined by Approximately 43% Between 1990 and 2024

Historical analysis identified a substantial long-term reduction in UK greenhouse gas emissions.

**Key result: Approximately 43% lower emissions in 2024 compared with 1990.**

Despite this progress, the historical series also shows fluctuations associated with major events, particularly during the COVID-19 period.

These findings illustrate the importance of analysing long-term patterns rather than relying exclusively on recent observations.

### 2. Forecast Models Project a Further 14–15% Reduction by 2029

Both the Standard Holt and Damped Trend models forecast continued reductions between 2025 and 2029.

The Damped Trend model projects:

**Approximately 14–15% lower emissions in 2029 compared with 2024.**

This suggests continued progress towards decarbonisation under the assumption that historical trends persist.

However, this is a statistical projection rather than a guarantee. Changes in energy policy, renewable energy adoption, economic activity and technology could materially alter future emissions.

### 3. Energy Supply Remains a Significant Emissions Contributor

Sector-level analysis identified the following shares in the project's 2024 emissions breakdown:

| Sector | Reported share |
|---|---:|
| Consumer expenditure | 26.0% |
| Transport and storage | 16.1% |
| Electricity, gas and steam supply | 14.9% |
| Manufacturing | 13.7% |
| Agriculture | 10.2% |

The analysis highlights electricity, gas and steam supply as a significant contributor to emissions.

This reinforces the importance of cleaner electricity generation, energy efficiency and investment in low-carbon infrastructure as part of broader decarbonisation efforts.

### 4. Emissions Are Concentrated Across Several High-Impact Activities

Industry-group analysis identified major emissions contributions from activities including:

- Consumer expenditure associated with travel and non-travel activities.
- Agriculture-related products and services.
- Air transport services.
- Gas, coal and other electricity production.
- Petroleum and natural gas production.

These findings indicate that emissions reduction requires coordinated improvements across energy production, transportation, manufacturing and consumer activity.

## Relevance to Renewable Energy & Net-Zero Transition

This project provides an analytical perspective on the challenges involved in achieving national climate targets.

Its findings are particularly relevant to the energy sector, where investment in renewable electricity generation, grid infrastructure and low-carbon technologies can contribute to reducing emissions.

Potential applications of similar analytical approaches include:

- **Decarbonisation monitoring:** Tracking historical emissions and assessing progress towards sustainability objectives.
- **Energy-sector analysis:** Identifying emissions-intensive activities and opportunities for cleaner energy solutions.
- **Forecasting and planning:** Using historical environmental data to develop baseline projections.
- **Data-driven decision-making:** Presenting complex sustainability datasets through accessible analytical visualisations.
- **Renewable energy strategy:** Providing broader emissions context for planning and evaluating the transition towards low-carbon electricity.

The project does not directly model renewable electricity generation, wind-farm performance or electricity grid operations. Instead, it provides national and sector-level emissions analysis relevant to the wider energy transition.

## Visualisations

The analysis includes three key visualisations:

**Figure 1 — Historical UK Emissions & Five-Year Forecast**

A time-series visualisation showing historical UK emissions from 1990 to 2024, alongside Standard and Damped Trend projections through 2029.

**Figure 2 — UK Greenhouse Gas Emissions by Sector (2024)**

A donut chart comparing the reported emissions contributions of major economic sectors.

**Figure 3 — Top 10 Highest-Emitting Industry Groups (2023)**

A horizontal bar chart highlighting the industry groups with the largest reported emissions.

Together, these visualisations communicate historical trends, forecast outcomes and sector-level emissions patterns.

## Limitations

While the analysis provides useful insights, several limitations should be considered.

**1. Historical data dependency**

The forecasting models use historical emissions observations rather than additional explanatory variables.

**2. External factors not modelled**

Future emissions may be influenced by renewable energy investment, government policies, economic conditions, technological development and changes in energy demand.

**3. Simplified forecasting approach**

Holt's method captures the overall level and trend but does not explicitly model relationships between different sectors or the effects of changes in economic activity.

**4. Data preprocessing assumptions**

Replacing suppressed non-numeric values with zeros introduces a potential source of uncertainty, particularly in more granular sector-level analysis.

**5. Forecast uncertainty**

The report does not present formal forecast confidence intervals or out-of-sample accuracy metrics. Forecasts should therefore be interpreted as illustrative projections, not validated predictions of future emissions.

## Future Improvements

The project could be expanded in several directions.

### Advanced Forecasting Models

Compare the existing statistical models with techniques such as:

- Random Forest Regression
- Long Short-Term Memory (LSTM) Neural Networks
- Multivariate Time-Series Forecasting

These approaches could help capture more complex relationships between emissions and their underlying drivers.

### Additional Data Sources

Incorporate explanatory variables such as:

- Renewable energy generation
- Electricity consumption
- National energy demand
- GDP and industrial output
- Climate and energy policy indicators

### Improved Data Quality & Model Evaluation

- Preserve missing and suppressed emissions values more accurately.
- Introduce time-based backtesting and forecasting accuracy metrics.
- Quantify forecast uncertainty through prediction intervals.
- Compare models across different historical periods.

### Interactive Analytics

Develop interactive visualisations to help users explore emissions trends across sectors, years and forecast scenarios.

## Running the Analysis

The project was developed in **Python using Jupyter Notebook**.

To explore the analysis:

1. Clone or download this repository.
2. Install the Python dependencies required by the notebook.
3. Open the Jupyter Notebook containing the analysis.
4. Ensure the source emissions dataset is available in the expected location.
5. Run the notebook cells to reproduce the data preparation, forecasting and visualisations.

Refer to the notebook for the specific implementation details and dependencies.

## Conclusion

The analysis highlights substantial progress in reducing UK greenhouse gas emissions over the past three decades.

Historical emissions declined by approximately **43% between 1990 and 2024**, while the Damped Trend model projects a further **14–15% reduction by 2029** relative to 2024.

Nevertheless, the findings illustrate the scale of the continued decarbonisation challenge, particularly across energy supply, transport and other emissions-intensive sectors.

By combining data preparation, time-series forecasting and sector-level analysis, this project demonstrates how data analytics can help interpret environmental trends and support informed discussion around sustainability and the transition towards a net-zero economy.

---

**Project Focus:** Python Data Analytics | Environmental Data Processing | Time-Series Forecasting | Greenhouse Gas Emissions | Renewable Energy | Net-Zero Transition
