# National Short Expiry & Salvage Monitoring System

A responsive, accessible management dashboard for monitoring short-expiry
commodities and salvage interventions in Zambia.

## Features

- Executive summary metrics calculated from batch-level records
- Clickable June-December expiry calendar
- Selectable historical bi-weekly snapshots
- Month-level batch detail and calculated salvage summaries
- Commodity profiles with intervention timelines
- Days-to-expiry warning centre
- Append-only salvaged commodities register
- Zambia Army initiative tracker
- Bi-weekly at-risk and cumulative-salvage trend
- Commodity value-at-risk Pareto ranking and top-10 list
- Lifecycle-stage KPIs and traffic-light action tracker
- Moving product scoreboard showing commodity, quantity, and value
- National Supply Chain Control Unit and Ministry of Health government header
- Searchable national expiry register with month, status, risk-band, and sort controls
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

Historical state is represented by two related structures:

- `snapshots`: aggregate position recorded at each bi-weekly review
- `salvageEvents`: append-only dated salvage transactions

Selecting a snapshot recalculates KPIs, monthly salvage progress, warning bands,
the Zambia Army opportunity, and the cumulative salvage register.

The national expiry register contains every commodity, batch, quantity, value,
expiry date, days to expiry, risk band, and current status. Search covers
commodity, batch, warehouse, province, facility, and engaged institution.

## Financial formulas

- `Total Value at Risk = SUM(Extended Price)`
- `Remaining Risk = Total Value at Risk - Total Salvaged Value`
- `Salvage Rate = Total Salvaged Value / Total Value at Risk * 100`
- `Extended Price = Total Units * Unit Price`

The current demonstration baseline uses:

- Total value at risk: `ZMW 33,836,176.68`
- Total salvaged: `ZMW 359,266.25`
- Remaining risk: `ZMW 33,476,910.43`
- Salvage rate: `1.06%`

The Zambia coat of arms asset is the public-domain SVG from
[Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Coat_of_arms_of_Zambia.svg).
