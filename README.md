# Energy Market Price Dynamics Analysis

This analysis examines real-world energy price data across major markets from December 1 to March 30, focusing on recent price acceleration.
The objective is to study how markets respond under a shock-driven environment, with emphasis on:

- persistence of upward price trends  
- magnitude of price adjustment across regions  
- differences in volatility across instruments  

The dataset reflects a non-stationary regime, where prices exhibit sustained directional movement rather than mean-reverting behavior.
As a result, the analysis prioritizes structural interpretation of price dynamics over traditional short-term return analysis.

## Problem Statement

Energy markets exhibit non-linear behavior driven by supply constraints, demand shocks, and structural frictions.

This project focuses on:

- analyzing sustained price trends
- quantifying total price growth across markets
- identifying differences in volatility and risk structure

## Data

The dataset contains weekly energy price series across:

- Italy (Petrol / Diesel)
- Germany (Petrol / Diesel)
- France (Petrol / Diesel)
- United States (Petrol / Diesel)

All series are:

- time-aligned and cleaned
- normalized to a base index (Base = 100)
- structured for cross-market comparison

## Methodology

- Data cleaning and normalization (Base = 100)
- Shock-aligned growth analysis
- Volatility estimation (standard deviation of returns)

## System Architecture

```
dashboard_project/
│── app.py        
│── engine.py     
│── plots.py      
│── config.py   
│── data.xlsx     
```

## Key Metrics

- Total price growth (%)
- Volatility (standard deviation of returns)
- Relative performance across markets

## Analytical Insights

### Shock Impact

The system exhibits a strong asymmetric response following the identified regime shift:

- US Diesel: +42.2%
- Germany Diesel: +32.7%
- US Petrol: +31.6%
- France Diesel: +26.7%
- Italy Diesel: +18.8%

Petrol markets show materially lower growth (≈ +6% to +18%), indicating uneven transmission across fuel types.

### Volatility Structure

Volatility analysis reveals a clear risk hierarchy:

- US Diesel: 0.062 (highest risk)
- Germany Diesel: 0.050
- US Petrol: 0.045

Diesel instruments consistently exhibit higher volatility, suggesting structurally elevated risk exposure.

### Structural Interpretation

**Diesel as a shock amplifier

Diesel markets show both higher volatility and stronger price increases.
This indicates that diesel acts as a primary transmission channel for macro and supply-side shocks, driven by its role in transportation and industrial activity.

**US market as a leading indicator

The US market demonstrates:

- faster price adjustment
- stronger acceleration
- higher volatility

European markets follow the same direction but with delayed response.

This suggests that the US acts as a **price discovery leader**, while EU markets behave as lagging responders.

**Asymmetric market response

Shock transmission is highly uneven:

* Italy Petrol: +6.2%
* US Diesel: +42.2%

This reflects structural fragmentation in energy pricing across regions and instruments.

## Structural Drivers 

The observed dynamics are consistent with a **supply-driven shock in global energy markets**.

Rather than attributing the movement to a single event, the behavior can be explained through underlying mechanisms:

- Supply-side constraints
  Energy prices respond sharply to disruptions in critical supply routes and production expectations

- Market structure differences
  US markets adjust faster due to more flexible pricing mechanisms
  EU markets exhibit slower but consistent alignment

- Fuel-type sensitivity
  Diesel reacts more strongly due to its direct linkage to logistics and industrial demand

The timing of the shift aligns with periods of increased geopolitical tension, reinforcing the interpretation of a supply-driven regime change.

## Practical Implications

- Diesel markets represent the primary source of volatility and risk  
- US pricing can serve as a leading indicator for global energy dynamics  
- Cross-market differences must be incorporated into pricing, hedging, and risk frameworks  

## Market Transmission Insight

The analysis reveals clear divergence in how price movements propagate across regions.

While most markets exhibit a consistent upward trend in diesel prices, the magnitude and speed of adjustment vary significantly.

Italy in particular shows relatively muted price increases and intermittent periods of stability compared to other regions.

This indicates that global energy price shocks are not transmitted uniformly. Instead, local market characteristics—such as regulatory structure, taxation regimes, and supply chain configuration—play a significant role in shaping the final price response.

Overall, the results highlight asynchronous adjustment dynamics and structural heterogeneity in energy price formation across markets.

## Tools & Stack

- Python
- Pandas
- Matplotlib
