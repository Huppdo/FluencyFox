# Tandem planning dashboard

Source for the Tandem planning dashboard (a Claude Dashboard artifact).

- `data/` holds the tabs of `tandem_data.xlsx` as CSV, plus `context.csv` with figures from the assessment brief (ARR, paying teams, price, capacity).
- `index.html` is the dashboard page. It runs inside the Dashboard artifact (it uses the `dash` and `d3` globals the artifact provides), so it won't render on its own.

Calculated figures (conversion rates, paid votes, ARR lost per month, consistency checks) are worked out in the page's `dash.calc` blocks.
