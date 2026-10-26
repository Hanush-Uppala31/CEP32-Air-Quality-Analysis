# India Air Quality Explorer (2020–2025)

An interactive, single-page website that analyses the `India_Air_Quality_2020_2025.csv` dataset:
monthly readings of seven pollutants (PM2.5, PM10, NO2, SO2, CO, NH3, Ozone) from 487 monitoring
stations in 255 cities across 31 states and union territories, January 2020 to December 2025.

## What the site covers

| Section | Question answered |
|---|---|
| Q1 | Average PM2.5 and PM10 concentration, compared with India's NAAQS limits |
| Q2 | Filter readings by monitoring station and date range (table, chart, CSV download) |
| Q3 | Missing pollutant values: how many, and optional median-filling per pollutant |
| Q4 | Averages grouped by region and season |
| Q5 | Trends over time and the ten highest states |
| Findings | Summary of what the data shows |

A global filter bar (region, state/UT, year range, median-fill switch) drives Q1, Q3, Q4 and Q5.

## Run it

It is a static site with no build step.

- **Locally:** open `index.html` in a browser (internet is needed for the Chart.js library and fonts).
- **GitHub Pages:** push this folder to a repository, then go to *Settings → Pages*, choose the
  `main` branch and the `/ (root)` folder, and save. The site appears at
  `https://<your-username>.github.io/<repository-name>/`.

## How it works

- The full dataset is embedded inside `index.html` in compact form, and every figure on the page
  is calculated in the browser from it. Nothing is hard-coded except the written findings.
- Charts use [Chart.js 4.4.1](https://www.chartjs.org/), loaded from cdnjs.
- Seasons follow the file's own labels: Winter (Dec–Feb), Summer (Mar–May),
  Monsoon (Jun–Sep), Post-Monsoon (Oct–Nov).
- Averages are the mean of monthly station averages. Missing values are excluded unless the
  median-fill switch is on, in which case each pollutant's own median is used.
- NAAQS reference limits (annual / 24-hour, µg/m³): PM2.5 40 / 60, PM10 60 / 100. The data holds
  monthly averages, so the annual limit is the fairer comparison.

## Data notes

- 245,448 rows = 487 stations × 7 pollutants × 72 months, with no duplicate rows.
- 9.01% of values are missing, evenly across years and seasons; NH3 has the most (15.2%), CO the fewest (4.5%).
- The file's `data_status` column labels every row "SYNTHETIC - NOT HISTORICAL OBSERVATIONS".
- The file gives no units; PM values are treated as µg/m³.

## Repository contents

```
index.html                              the website
data/India_Air_Quality_2020_2025.csv    source dataset
README.md                               this file
```
