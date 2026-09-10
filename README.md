# Plan Crime Resources Around High-Risk Times

## An analysis of Chicago crime trends, rush hours, holidays, and seasonal patterns

**Author**: Siwar Ehwass

## Business Problem

Chicago public safety teams need to understand when reported crime is more likely to increase. This project studies past crime reports to identify long-term trends, busy times of day, high-count holidays, and repeating seasonal patterns. These findings can support better planning and help city teams prepare before demand increases.

## Data

- **Source**: [Chicago Police Department: Crimes from 2001 to Present](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2/about_data)
- **Time range**: January 1, 2001 to September 3, 2026
- **Size**: 8,627,693 reported crimes
- **Main information used**: date, time, and crime type
- **Added information**: the name of the US holiday, when a crime occurred on a holiday

The 2026 data is incomplete. For this reason, the yearly comparison uses complete years from 2001 through 2025.

## Methods

- Combined 26 yearly data files into one dataset.
- Defined AM rush hour as 7:00 AM to before 10:00 AM and PM rush hour as 4:00 PM to before 7:00 PM.
- Matched each date with the US holiday calendar.
- Used seasonal decomposition to find weekly and yearly patterns. The seasonality analysis used the ten most recent complete years, from 2016 through 2025.
- **Forecasting method**: 

## Results

### Reported Crime Has Decreased Over Time

![Chicago crime over time](visuals/chicago_crime_over_time.png)

> Reported crime decreased by **51.1%**, from 485,974 reports in 2001 to 237,695 reports in 2025. However, 11 crime types increased over the same period, so the overall decrease does not apply to every type of crime.

### Crime Follows a Yearly Pattern

![Yearly seasonal pattern](visuals/yearly_seasonal_pattern.png)

> Reported crime follows a repeating yearly pattern. Crime is usually highest in **July** and lowest in **February**. This suggests that seasonal demand should be considered when planning resources.

### PM Rush Hour Has More Reported Crime

![AM and PM rush-hour crime](visuals/am_pm_rush_hour.png)

> PM rush hour had **1,352,388** reported crimes, compared with **863,343** during AM rush hour. PM rush hour had 489,045 more reports. Motor vehicle theft was also more common during PM rush hour.

### New Year's Day Has the Highest Holiday Count

![Holidays with the most reported crime](visuals/top_holidays.png)

> **New Year's Day** had the highest number of reported crimes among US holidays, with 37,240 reports. Independence Day and Labor Day were the next two highest.

## Model

`[The forecasting model has not been completed yet. Add the final model name, what it predicts, the forecast period, and how it was tested.]`

### Forecast Compared with Actual Crime

**Key metrics**

> 

## Recommendations

- Plan more staff and prevention resources for PM rush hour, when reported crime is higher than during AM rush hour.
- Prepare additional coverage for July and begin planning before the summer increase.
- Review staffing needs around New Year's Day, Independence Day, and Labor Day.
- Continue tracking the crime types that increased even while total reported crime decreased.

## Limitations and Next Steps

- The data includes reported crimes only. Some crimes may not be reported.
- The analysis shows patterns, but it does not prove that rush hour, holidays, or seasons cause crime.
- Holiday totals are combined across many years and may be affected by changes in reporting and holiday-calendar rules.
- The current analysis predicts neither specific crime types nor neighborhoods.
- The next step is to build and test a forecasting model, then compare predicted monthly crime with actual monthly crime.
- Future work could forecast crime by neighborhood or crime type to support more focused planning.

## Project Links

- [View the analysis notebook](notebooks/02_crime_analysis.ipynb)
- [View the visuals folder](https://github.com/swirita/Chicago-Crime-Analysis-and-Forecasting/tree/main/visuals)
- [View the original data source](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2/about_data)

## For Further Information

The full notebook includes the top crime types during each rush hour, the top crime types on the three highest-count holidays, the crime types that moved against the overall trend, and additional seasonal patterns.

For any additional questions, please contact **[add email address]**.
