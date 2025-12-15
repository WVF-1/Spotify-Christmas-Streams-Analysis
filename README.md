# Spotify-Christmas-Streams-Analysis
An Analysis of streams per Christmas song, from Spotify data, over the Christmas season. Utilized Prophet modeling techniques to forecast the future views, as well as simulated the impact of a new breakout hit Christmas song, on the current leaderboard's market share.

## Project Objectives
- Analyze historical Christmas music streaming patterns
- Forecast total Christmas streaming volume for 2026 using Prophet
- Identify which tracks are likely to dominate future Christmas seasons
- Simulate the impact of a new breakout Christmas song on the existing ecosystem
- Demonstrate best practices in time series modeling and validation

## Dataset Description
The dataset contains weekly Spotify streaming data for popular Christmas songs from 2017 to 2025. Key variables include:
- Track name
- Artist
- Weekly stream counts
- Week of year
- Calendar year
The analysis focuses on weeks 46–52 to capture the core Christmas listening period.
You may view the dataset here: [Kaggle Dataset](https://www.kaggle.com/datasets/jonassouza872/christmas-hits-daily-streaming-history-2017-2025).

## Exploratory Data Analysis (EDA)
Exploratory analysis was performed to understand distributional patterns and seasonal structure within the data. Key steps include:
- Distribution analysis of streams by artist and track
- Seasonal heatmaps highlighting recurring Christmas spikes
- Histograms examining:
  - Artist-level popularity
  - Track-level dominance
  - Weekly streaming intensity
- Correlation analysis between temporal features
These analyses confirm strong annual seasonality and justify the use of time series models.

## Time Series Forecasting with Prophet
Facebook Prophet is used to forecast total Christmas-season streams into 2026. The model incorporates:
- Yearly seasonality
- Holiday effects
- Trend changepoint regularization
The forecasting process is intentionally iterative, documenting initial misalignment and subsequent refinements to improve realism and seasonal accuracy.

## Model Validation
Model performance is evaluated using rolling-origin cross-validation. This method:
- Trains the model on historical Christmas seasons
- Forecasts the following season
- Repeats the process across multiple years
This validation approach mirrors real-world forecasting conditions and provides reliable error metrics such as MAE, and RMSE.

## Ecosystem Modeling and Scenario Simulation
Beyond forecasting, this project models Christmas streaming as a finite attention market. The central assumption is that total Christmas listening volume is limited, and that new songs redistribute attention rather than purely increasing it.

To explore this, a hypothetical new Christmas song is introduced and evaluated under multiple market share capture scenarios.

## Scenario Analysis: New Song Market Share
The impact of a new song is simulated across the following market share scenarios:
- 1%: Niche seasonal hit
- 5%: Strong breakout
- 10%: Modern Christmas classic
- 15–25%: Mariah-tier disruption
For each scenario:
- Existing tracks lose market share proportionally
- Rankings and projected stream counts are recalculated
- Ecosystem-level shifts are visualized and compared
This scenario sweep functions as a conceptual slider, allowing readers to observe how competitive dynamics change under increasing disruption.

## Key Findings
- Christmas music exhibits extreme but predictable seasonality
- Legacy tracks remain dominant under low-disruption scenarios
- A new song must capture approximately 10% or more of seasonal attention to rival established classics
- Scenario-based modeling provides deeper insight than point forecasts alone

## Tools and Libraries
- Python
  - pandas
  - NumPy
  - matplotlib
  - seaborn
  - Prophet

### About Building Data Together
Building Data Together is a weekly data science newsletter focused on transparent modeling, practical analytics, and learning through real-world datasets.

# Final Notes
This project emphasizes modeling process, validation, and assumption-driven analysis rather than purely predictive performance. The goal is to demonstrate how thoughtful modeling choices lead to clearer insights and more interpretable results.
