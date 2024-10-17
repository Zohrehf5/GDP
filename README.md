# Forecasting GDP in United States


Gross Domestic Product (GDP) is critical indicators of the economic health and stability of the United States. GDP measures the total value of goods and services produced, representing overall economic growth. Accurate GDP forecasts help governments, businesses, and investors anticipate future economic conditions and plan accordingly. Historical examples demonstrate the impact of GDP forecasts on shaping major U.S. policy responses:
•	**2008 Financial Crisis:** Early GDP forecasts showed a sharp economic contraction, prompting the U.S. government to implement the **$700 billion Troubled Asset Relief** Program (TARP) to stabilize the banking system and prevent a prolonged recession.
•	**Post-World War II Economic Boom:** Positive GDP forecasts predicted strong post-war growth, leading to transformative policies like the **G.I. Bill** and large-scale infrastructure projects, which fueled decades of economic expansion.
•	**COVID-19 Pandemic:** As GDP forecasts in early 2020 predicted significant economic declines due to lockdowns, the U.S. government passed the **CARES Act**, a $2.2 trillion stimulus package, to mitigate the economic fallout.
These cases illustrate the strategic importance of GDP forecasts in shaping timely and impactful policy interventions, underscoring the need for reliable economic predictions.

## Code structure

├── data
│   ├── CPIAUCSL.csv: https://fred.stlouisfed.org/series/CPIAUCSL The Consumer 
│   ├   			Price Index for All Urban Consumers.
│   ├── GDP.csv: https://fred.stlouisfed.org/series/GDP
│   ├── INDPRO.csv: https://fred.stlouisfed.org/series/INDPRO The Federal Reserve's 
│   ├ 			monthly index of industrial production
│   ├── URATE.csv: https://fred.stlouisfed.org/series/UNRATE Unemployment Rate 
│   ├── DFF.csv:  https://fred.stlouisfed.org/series/DFF  Effective Federal Funds Rate 
│   ├── FEDFUNDS.csv: https://fred.stlouisfed.org/series/FEDFUNDS Targeted Federal 
│   ├ 			Funds Rate│   
│   
├── GDP.ipynb
│   
├── image
│   ├── pic1.png
│   └── pic2.png
│   
├── README.md
├── Forecasting GDP.docx- Detail report for this project.
└── .gitignore

## Results and evaluation
In this project, we explored the use of various machine learning models to forecast GDP, leveraging both time series analysis and advanced modeling techniques. The models, including Decision Trees, Random Forest, Gradient Boosting, and SARIMA, performed exceptionally well, with R² scores nearing perfection in most cases. This indicates that the features used, such as CPIAUCSL, FEDFUNDS, and INDPRO, have strong predictive power for U.S. GDP trends.
The SARIMA model effectively captured both the trend and seasonality in the GDP data, which was validated by significant P-values for key components like the seasonal moving average term. However, the presence of heteroskedasticity, as indicated by the Prob(H) test, suggests that model reliability might decrease in periods of high volatility, warranting further analysis and refinement.

## Future work
1.	Refining the SARIMA Model: Given the presence of heteroskedasticity in the residuals, a more advanced model, such as GARCH (Generalized Autoregressive Conditional Heteroskedasticity), could be explored to better handle the volatility in the data. This could improve the model's forecast accuracy during turbulent economic periods.
2.	Adding Exogenous Variables (SARIMAX): Future work could involve incorporating additional exogenous variables, such as interest rates, inflation, or global economic indicators, using the SARIMAX model. This would allow the model to capture external factors that may influence GDP, potentially leading to more accurate predictions.
3.	Exploring Non-linear Models: Although tree-based models like Random Forest and Gradient Boosting performed well, exploring non-linear models such as Neural Networks or Long Short-Term Memory (LSTM) networks might yield better results, particularly for capturing complex, non-linear relationships in time series data.
4.	Cross-Validation with Time-Series Splits: Implementing rolling-window cross-validation or time series split validation will provide a more robust evaluation of the models' ability to generalize to future, unseen data. This method would help ensure the model's stability over different time periods.
5.	Scenario Analysis and Stress Testing: Incorporating scenario analysis by simulating different economic conditions (e.g., a financial crisis or a rapid recovery) could provide deeper insights into the model’s behavior under varying economic circumstances. This could assist policymakers in understanding potential GDP trajectories under different future scenarios.
By taking these steps, the models can be further improved, allowing for more reliable and actionable GDP forecasts. These forecasts would continue to provide valuable insights for policymakers, businesses, and investors in their decision-making processes.



