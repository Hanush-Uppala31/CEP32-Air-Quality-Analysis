# CEP-32 Air Quality Explorer — redesigned static site

## Included
- `index.html`, `style.css`, `script.js`
- `India_Air_Quality_2020_2025.csv` (dataset supplied for this redesign)

## Run locally
Keep all four files in the same folder. For the most reliable CSV loading, open the folder in VS Code and use the Live Server extension, or publish the files through GitHub Pages.

## Publish to your existing GitHub Pages repository
1. Download and extract this ZIP.
2. Open your repository: https://github.com/Hanush-Uppala31/CEP32-Air-Quality-Analysis
3. Back up the current files.
4. Upload/replace `index.html`, `style.css`, `script.js`, and `India_Air_Quality_2020_2025.csv` in the repository root.
5. Commit the changes and wait for GitHub Pages to rebuild.

## Important data note
The supplied CSV is labelled synthetic/date-adjusted. The dashboard preserves that warning. The monthly trend charts are useful for demonstrating the interface and analysis workflow, but must not be described as actual historical CPCB measurements.


UPLOAD NOTE: The CSV has been reduced to PM2.5 and PM10 only to fit GitHub browser upload limits while retaining all locations and monthly dates in this synthetic dataset. These are illustrative synthetic/date-adjusted values, NOT official historical CPCB observations.
