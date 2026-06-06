# National Short Expiry & Salvage Monitoring System

A responsive, accessible management dashboard for monitoring short-expiry
commodities and salvage interventions in Zambia.

## Features

- Nine-page dashboard architecture with responsive left navigation
- Dedicated Executive Summary, Expiry Forecast, Commodity Register, Warning
  Centre, Salvage Tracker, Action Tracker, Root Cause Analysis, Historical
  Snapshots, and Institution Performance views
- Executive summary metrics calculated from batch-level records
- Shared June-December expiry calendar visible on every dashboard page
- Selectable historical bi-weekly snapshots
- Month-level batch detail and calculated salvage summaries
- Commodity profiles with intervention timelines
- Days-to-expiry warning centre
- Append-only salvaged commodities register
- Zambia Army initiative tracker
- Bi-weekly at-risk and cumulative-salvage trend
- Commodity value-at-risk Pareto ranking and top-10 list
- Lifecycle-stage KPIs and traffic-light action tracker
- Side-to-side product scoreboard showing commodity, quantity, value, and expiry date
- National Supply Chain Control Unit and Ministry of Health government header
- Searchable national expiry register with month, status, risk-band, and sort controls
- Responsive layout for desktop, tablet, and mobile
- Print-friendly reporting view
- Automated deployment to GitHub Pages

## Run locally

Open `index.html` directly in a browser. No build step or package installation is
required.

## Data note

The dashboard is loaded from `Short dated products.xlsx` and
`Salvaged Products-Merged_May26.xlsx`. It contains 116 supplied short-dated
product rows for June-September 2026 and detailed May-July shipment evidence.
Fields absent from the source workbooks remain blank.

Historical state is represented by two related structures:

- `snapshots`: aggregate position recorded at each bi-weekly review
- `salvageEvents`: append-only dated salvage transactions

Selecting a snapshot recalculates KPIs, monthly salvage progress, warning bands,
the Zambia Army opportunity, institution performance, executive alerts, and the
cumulative salvage register across all dashboard pages.

The national expiry register contains every commodity, batch, quantity, value,
expiry date, days to expiry, risk band, and current status. Search covers
commodity, batch, warehouse, province, facility, and engaged institution.

## Financial formulas

- `Total Value at Risk = SUM(Extended Price)`
- `Remaining Risk = Total Value at Risk - Total Salvaged Value`
- `Salvage Rate = Total Salvaged Value / Total Value at Risk * 100`
- `Extended Price = Total Units * Unit Price`

The supplied priced May-July summary uses:

- Total value at risk: `ZMW 49,725,881.51`
- Total salvaged: `ZMW 4,177,687.58`
- Remaining risk: `ZMW 45,548,193.93`
- Salvage rate: `8.40%`

The Zambia coat of arms asset is the public-domain SVG from
[Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Coat_of_arms_of_Zambia.svg).
