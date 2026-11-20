---
title: Las Vegas Weather Analysis
---

[Back to Portfolio](./)

# Las Vegas Weather Analysis

**Tools:** Python, pandas, and Matplotlib

## What I built

I wrote a Python program to analyze daily observations from the Las Vegas Weather Forecast Office from 1997 through 2025. It makes three charts: estimated annual average temperature, the number of days each year with a high of at least 100°F, and average rainfall by month.

I estimated the daily mean temperature using the day's high and low. If a measurement was missing, I left it missing rather than counting it as zero. This matters for rainfall in particular: a day with no reported measurement isn't necessarily a day with no rain.

## How to run it

Open a terminal in the folder containing `main.py` and `LasVegasWeather.csv`. Then run:

```powershell
python -m pip install pandas matplotlib
python main.py
```

The program writes three PNG charts: `temperature.png`, `hot_days.png`, and `rainfall.png`.
