# Marketing Campaign Performance Dashboard

A modern campaign analytics project that combines a browser-based executive dashboard and a Python data generator to simulate and visualize digital marketing results.

## What this project does

This repository supports a campaign performance showcase by:

- generating realistic synthetic marketing campaign records with `scripts/generate_data.py`
- cleaning and validating campaign data in CSV format
- displaying campaign KPIs in a web dashboard under `docs/`
- enabling interactive analysis by platform, region, campaign type, audience, and ROI

## Dataset overview

The dataset is synthetic and designed to mirror the structure of real marketing performance data:

- raw campaign file: `data/campaign_data.csv`
- cleaned dataset: `data/cleaned_campaign_data.csv`
- dashboard source: `docs/data.json`

Key fields include campaign metadata, impressions, clicks, CTR, leads, conversions, spend, revenue, ROI, CPC, CPM, and customer acquisition cost.

## Data preparation and validation

The data workflow includes:

- generating campaign records with Python and NumPy
- filling missing numeric values using median imputation
- replacing missing categorical values with the most common label
- deduplicating records
- standardizing date formats, platform labels, and audience segments
- validating the dataset structure and KPI calculations

## Dashboard capabilities

The dashboard in `docs/index.html` features:

- executive-style KPI cards for revenue, profit, ROI, and campaign health
- cross-filters for platform, region, campaign type, audience segment, and ROI status
- charts and matrix views powered by Chart.js
- a dedicated strategy panel for executive insights
- a responsive interface for campaign filtering and performance review

## Key benefits

This project is useful for:

- marketing teams reviewing campaign effectiveness
- agencies preparing client performance summaries
- growth teams analyzing channel ROI
- product marketers measuring launch success
- executives making budget allocation decisions

## Repository structure

- `docs/`
  - `index.html` — web dashboard UI
  - `style.css` — dashboard styling and layout
  - `script.js` — interactive logic, filtering, and Chart.js rendering
  - `data.json` — processed campaign records for the dashboard
- `data/`
  - `campaign_data.csv` — raw generated campaign data
  - `cleaned_campaign_data.csv` — dataset after cleaning and validation
- `scripts/`
  - `generate_data.py` — generates and cleans campaign data
- `requirements.txt` — Python library requirements
- `LICENSE` — project license

## Setup

Install the Python dependencies before running data generation:

```bash
pip install -r requirements.txt
```

## Running locally

### Start the dashboard

The dashboard loads `docs/data.json` via browser fetch, so it is best viewed through a local server.

```bash
cd docs
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

### Regenerate data

To recreate the campaign dataset:

```bash
python scripts/generate_data.py
```

## License

This project is released under the MIT License. See the `LICENSE` file for full terms.
