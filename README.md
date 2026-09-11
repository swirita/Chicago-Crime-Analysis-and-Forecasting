# Plan Crime Resources Around High-Risk Times

## Chicago crime patterns and six-month forecasts for better resource planning

**Author**: Siwar Ehwass

## Business Problem

Chicago law enforcement must allocate personnel and prevention resources across periods of changing demand. Historical crime reports are analyzed to identify long-term trends, rush-hour differences, holiday peaks, and seasonal patterns. Theft and Battery counts are also forecasted for the next six months to support staffing and resource-allocation decisions.

## Data

* **Source**: [Chicago Police Department: Crimes from 2001 to Present](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2/about_data)
* **Time range**: January 1, 2001 to September 3, 2026
* **Size**: 8,627,693 reported crimes
* **Main information used**: date, time, and crime type
* **Added information**: US holiday name

Since 2026 is incomplete, I used complete years from 2001 through 2025 for the yearly comparison.

## Methods

* Combined 26 yearly crime files.
* Compared crime during AM and PM rush hours.
* Matched crime dates with the US holiday calendar.
* Used seasonal decomposition to study weekly and yearly patterns.
* Created monthly Theft and Battery time series.
* Checked stationarity and used ACF and PACF plots to choose initial models.
* Compared manually selected models with tuned Auto ARIMA models.
* Tested each model on the final six months of known data.
* Used the complete time series to forecast six new months.

## Results

### Reported Crime Has Decreased Over Time

![Chicago crime over time](visuals/chicago_crime_over_time.png)

> Reported crime decreased by **51.1%**, from 485,974 reports in 2001 to 237,695 in 2025. However, 11 crime types increased during the same period, so the overall decrease does not tell the full story.

### Crime Follows a Yearly Pattern

![Yearly seasonal pattern](visuals/yearly_seasonal_pattern.png)

> Reported crime usually reaches its highest point in **July** and its lowest point in **February**. Planning for the summer increase should begin before July.

### PM Rush Hour Has More Reported Crime

![AM and PM rush-hour crime](visuals/am_pm_rush_hour.png)

> PM rush hour had **1,352,388** reported crimes, compared with **863,343** during AM rush hour. Motor vehicle theft was also more common during PM rush hour.

### New Year’s Day Has the Highest Holiday Count

![Holidays with the most reported crime](visuals/top_holidays.png)

> **New Year’s Day** had the highest holiday crime count, followed by Independence Day and Labor Day.

## Forecasting Results

### Theft Forecast

I compared a manually selected seasonal model with a tuned Auto ARIMA model. The manual model performed better on unseen data, so I selected it for the final Theft forecast.

* **Average monthly error**: approximately 262 crimes
* **Average percentage error**: **6.17%**

![Theft forecast for the next six months](visuals/theft_forecast_next_6_months.png)

> Theft is forecasted to decrease from approximately **4,124 crimes** in the first forecast month to **3,093 crimes** in the final month. This is a predicted decrease of approximately **1,030 crimes**, or **24.99%**.

### Battery Forecast

* **Selected model**: `[Add final Battery model]`
* **Average monthly error**: `[Add Battery MAE]`
* **Average percentage error**: `[Add Battery MAPE]`

`![Battery forecast for the next six months](visuals/battery_forecast_next_6_months.png)`

> Battery is forecasted to change from **[beginning count]** to **[final count]** crimes. This is a net change of **[raw change]** crimes, or **[percentage change]%**.

## Recommendations

* Put more staff and prevention resources into PM rush hour, where reported crime is much higher.
* Prepare for the yearly increase before July instead of reacting after crime has already risen.
* Review coverage around New Year’s Day, Independence Day, and Labor Day.
* Theft is forecasted to decrease, but this should not be treated as a reason to make large resource cuts. The forecast still has uncertainty.
* Compare the final Theft and Battery forecasts to decide which crime needs the larger share of flexible resources.
* Update the forecast every month as new reports become available.

## Limitations and Next Steps

* The dataset includes reported crimes only.
* These patterns show when crime is higher, but they do not prove what caused it.
* The forecasts cover Chicago as a whole and do not show which neighborhoods need the most support.
* Weather, major events, policy changes, and other outside factors were not included.
* A useful next step would be forecasting by district and time of day for more focused resource planning.

## Project Links

* [View the analysis notebook](notebooks/02_crime_analysis.ipynb)
* [View the forecasting notebook](notebooks/03_crime_forecasting.ipynb)
* [View the visuals folder](https://github.com/swirita/Chicago-Crime-Analysis-and-Forecasting/tree/main/visuals)
* [View the original data source](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2/about_data)

## For Further Information

For any questions, contact **[siwarehwass@gmail.com](mailto:siwarehwass@gmail.com)**.
