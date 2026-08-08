# Campaign Performance Dashboard

A marketing analytics dashboard that visualizes campaign performance across platforms, regions, and audience segments using synthetic campaign data.

## Overview

This project includes a browser-based dashboard built with HTML, CSS, and JavaScript, plus a Python data generator for synthetic campaign performance records. The dashboard presents key metrics such as revenue, ROI, campaign spend, conversions, and audience performance.

## Features

- Interactive campaign performance dashboard (`docs/index.html`)
- Metric tiles for revenue, profit, ROI, and campaign health
- Platform, region, campaign type, audience segment, and ROI filters
- Multiple dashboard panels for spend/revenue, regional and audience insights, funnel efficiency, and executive summary
- Synthetic campaign dataset generation and cleaning script

## Project Structure

- `docs/`
  - `index.html` — main dashboard page
  - `style.css` — dashboard styling
  - `script.js` — dashboard interaction and Chart.js visualizations
  - `data.json` — sample campaign dataset used by the dashboard
- `data/`
  - `campaign_data.csv` — campaign dataset file
  - `cleaned_campaign_data.csv` — cleaned dataset output
- `scripts/`
  - `generate_data.py` — synthetic campaign data generation and cleaning script
- `requirements.txt` — Python dependencies for data generation

## Requirements

- Python 3.x
- Chrome, Edge, Firefox, or another modern browser for viewing the dashboard

Python dependencies:

- pandas
- numpy
- matplotlib
- seaborn
- plotly
- openpyxl
- scikit-learn

Install dependencies with:

```bash
pip install -r requirements.txt
```

## Usage

### Run the dashboard

1. Open `docs/index.html` directly in your browser.
2. If using local data from `docs/data.json`, the dashboard will load the sample campaign dataset automatically.
3. Use the filter controls to explore campaigns by platform, region, campaign type, audience, and profitability.

### Generate or refresh campaign data

Run the data generator script to create or update the campaign dataset:

```bash
python scripts/generate_data.py
```

The script builds synthetic campaign records and applies basic cleaning before saving generated output.

## Notes

- The dashboard currently uses Chart.js for visualizations.
- The sample dataset in `docs/data.json` includes campaign KPIs such as impressions, clicks, CTR, leads, conversions, spend, revenue, ROI, CPC, CPM, and customer acquisition cost.

## License

This project does not include a license file. Add one if you want to share or publish the dashboard.
