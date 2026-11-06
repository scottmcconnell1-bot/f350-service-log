# F-350 Service Log

Maintenance tracker for Scott's 2013 Ford F-350 Super Duty Lariat (6.7L Power Stroke diesel).

- **Upcoming**: what's due, from the 6.7L diesel schedule and the truck's driving rate, plus a 3-year forecast of shop visits.
- **History**: every record since 2013 (CARFAX, invoices, DIY jobs), searchable, with receipts attached.
- **Schedule**: the intervals used, Normal and Severe.

## How it works

This repo holds only the website (`index.html`), served by GitHub Pages. The records and receipt files live in a separate **private** repo (`f350-service-data`). The page reads and writes that repo directly from your browser using a fine-grained GitHub token that you paste into **Settings** once per device. The token is kept in that browser's local storage and is never committed anywhere.

Receipt auto-fill calls the Anthropic API with your own key (optional, also stored only in your browser).

## Setup on a new device

1. Open the site and click **Settings**.
2. Paste a fine-grained token with **Contents: Read and write** on `f350-service-data` only.
3. Optionally paste an Anthropic API key.
4. Click **Connect**.
