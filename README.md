# ZAMMSA Short Expiry & Salvage Dashboard

A responsive, accessible management dashboard for monitoring short-expiry
commodities and salvage interventions in Zambia.

## Features

- Executive summary metrics calculated from batch-level records
- Clickable June-December expiry calendar
- Month-level batch detail and calculated salvage summaries
- Commodity profiles with intervention timelines
- Automatic critical, moderate, and controlled risk alerts
- Bi-weekly at-risk and cumulative-salvage trend
- Responsive layout for desktop, tablet, and mobile
- Print-friendly reporting view
- Automated deployment to GitHub Pages

## Run locally

Open `index.html` directly in a browser. No build step or package installation is
required.

## Data note

The current June-December 2026 monthly values and batch records are a
demonstration dataset implementing the supplied control-tower concept. Replace
them with the validated national commodity line list before operational use.
All month totals, salvage values, remaining risk, salvage rates, and alerts are
calculated from the batch records in `index.html`.
