# West Africa Data Pipeline

A synthetic data pipeline and dashboard for infrastructure, trade, and economic indicators across West African countries.

Link 🔗 - https://dashboard-amber-beta.vercel.app/

## Overview

This project generates plausible synthetic datasets for 18 West African countries (+ external comparators) across multiple dimensions:

- **Infrastructure quality** (AfDB‑style indices)
- **Trade flows** (UN Comtrade, WITS)
- **Macroeconomic indicators** (IMF, World Bank)
- **Financial‑zone effects** (FTZ impact simulations)

The data is used to power a React/Next.js dashboard for visualization and to train a Graph Neural Network (GNN) for cross‑country spillover prediction.

## Structure

- `collectors/` – Modular data collectors (AfDB, IMF, World Bank, UN Comtrade, WITS)
- `core/` – Shared utilities, caching, configuration
- `dashboard/` – Next.js frontend (Vercel‑deployed)
- `gnn/` – Graph Neural Network for spillover modeling
- `signals/` – Derived indicators (growth, risk, integration)
- `viz/` – Plotting and map utilities
- `data/` – Generated CSV/Parquet outputs
- `scripts/` – ETL and simulation scripts

## Key Features

- **Synthetic but realistic** – Anchored to known baselines, with realistic noise and trends.
- **Multi‑source** – Harmonizes data from 5+ international organizations.
- **Graph‑based modeling** – Countries as nodes, trade/infrastructure as edges.
- **Dashboard** – Interactive maps, time‑series, cross‑country comparisons.
- **FTZ impact analysis** – Simulates effects of proposed Free Trade Zones.

## Usage

1. Install dependencies: `pip install -r requirements.txt`
2. Run collectors: `python -m collectors.scheduler`
3. Generate signals: `python -m signals.compute`
4. Launch dashboard: `cd dashboard && npm run dev`

## Report

See `WestAfrica_FTZ_Findings_Report.docx` for detailed analysis of Free Trade Zone potential and infrastructure gaps.

## Purpose

Built for research on regional integration, investment targeting, and policy simulation in West Africa. The synthetic approach allows stress‑testing scenarios without sensitive real data.

Link - https://github.com/Meugenn/west-africa-data

## License

Internal research tool. Contact for collaboration.
