# FlipIQ: AI-Powered House Flip Opportunity Detection

> **Autonomous agent system that identifies high-potential real estate flip opportunities using Zillow data, predictive scoring, and proactive market intelligence.**

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://python.org)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.30+-red.svg)](https://streamlit.io)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Demo](https://img.shields.io/badge/Demo-Available-brightgreen.svg)](#try-the-demo)
[![Beta](https://img.shields.io/badge/Beta-Signups_Open-orange.svg)](landing_page.html)

---

## Current Status: Customer Validation

**We're currently validating FlipIQ with real house flippers.** This MVP demonstrates the technical capability and value proposition. We're talking to investors to validate product-market fit before scaling.

### Validation Goals
- 50 customer discovery conversations
- 20 demo calls
- 100 landing page signups
- Determine: **Will flippers pay for AI-powered opportunity detection?**

See our full validation strategy: [`docs/CUSTOMER_VALIDATION.md`](docs/CUSTOMER_VALIDATION.md)

---

## Try the Demo

## Live Dashboard

🚀 **[Try the Live Dashboard →](https://flipiq.streamlit.app/)**

Fully interactive demo analyzing 26,000+ ZIP codes. No installation required.

## Landing Page

📄 **[View Marketing Page →](https://abpuri.github.io/flipiq/landing_page.html)**

Features:
- ROI calculator
- Feature comparison
- Signup form
- FAQ

---

## The Problem

House flippers spend **40+ hours per month** manually researching markets across fragmented tools, missing **80% of emerging opportunities** due to reactive workflows. Current solutions require constant monitoring and provide historical data—not actionable intelligence.

## The Solution

FlipIQ is an **AI-powered opportunity detection platform** that deploys autonomous agents to monitor 26,000+ US ZIP codes, score opportunities using a proprietary 5-factor model, and proactively alert investors to high-potential markets **30-60 days before competitors**.

### Key Differentiator

| Them | Us |
|------|-----|
| You search for opportunities | Opportunities come to you |
| Reactive tools | Proactive intelligence |
| Historical data | Predictive scoring |
| Manual analysis | AI-powered automation |

---

## Key Features

- **Proactive Alert System** — HOT/WARM/WATCH priority notifications based on customizable thresholds
- **5-Factor Scoring Engine** — Composite scores combining appreciation, velocity, distress, pricing power, and value gap
- **6 Autonomous Agents** — End-to-end workflow automation from data refresh to report generation
- **Interactive Dashboard** — 6-tab Streamlit interface for analysis, visualization, and deep-dives
- **Property Deep Dive** — Comprehensive analysis with trend, momentum, risk, and investment recommendations

---

## Project Highlights

| Metric | Value |
|--------|-------|
| ZIP Codes Analyzed | **26,307** |
| Autonomous Agents | **6** |
| Simulation Period | **90 days** |
| Alerts Generated | **538** (171 HOT, 367 WARM) |
| Scoring Factors | **5** |
| Dashboard Tabs | **6** |
| Strategy Presets | **3** (Fast Flip, Value-Add, Balanced) |

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| **Language** | Python 3.9+ |
| **Data Processing** | Pandas, NumPy |
| **Machine Learning** | Scikit-learn (normalization, scoring) |
| **Visualization** | Plotly, Matplotlib, Seaborn |
| **Dashboard** | Streamlit |
| **Architecture** | Agent-based orchestration pattern |
| **Data Source** | Zillow Research (public datasets) |

---

## Repository Structure

```
zillow/
├── data/
│   ├── raw/zillow/                  # Original Zillow CSV datasets
│   └── processed/
│       ├── agent_logs/              # Simulation outputs
│       └── *.csv                    # Scored opportunities
│
├── src/
│   ├── data_loader.py               # Dataset loading
│   ├── scoring_engine.py            # 5-factor scoring
│   ├── agent_workflow.py            # 6 agents + orchestrator
│   ├── property_analyzer.py         # Deep-dive analysis
│   └── alert_system.py              # Alert generation
│
├── workflows/
│   └── simulate_agent_run.py        # Agent simulation
│
├── notebooks/                       # Jupyter notebooks
│
├── docs/
│   ├── architecture.md              # System architecture
│   ├── DEMO.md                      # Demo walkthrough
│   ├── DEPLOYMENT.md                # Deployment guide
│   ├── CUSTOMER_VALIDATION.md       # Validation strategy
│   │
│   ├── customer_discovery/          # Customer research materials
│   │   ├── outreach_templates.md    # Email/LinkedIn templates
│   │   ├── discovery_call_script.md # Call scripts
│   │   └── feedback_tracker_template.csv
│   │
│   ├── demo/                        # Demo materials
│   │   ├── demo_script.md           # Video script
│   │   ├── presentation_deck.md     # Slides content
│   │   └── one_pager.md             # Leave-behind
│   │
│   ├── value_props/                 # Sales materials
│   │   ├── use_cases.md             # Customer stories
│   │   ├── competitive_analysis_one_pager.md
│   │   └── roi_examples.md          # ROI calculations
│   │
│   ├── market_analysis.md           # TAM/SAM/SOM
│   ├── unit_economics.md            # LTV, CAC, pricing
│   ├── financial_projections.md     # 3-year model
│   ├── investor_pitch_deck_content.md
│   ├── investor_memo.md             # Investment memo
│   └── risk_analysis.md             # Risk assessment
│
├── streamlit_app.py                 # Main dashboard
├── landing_page.html                # Marketing page
└── requirements.txt                 # Dependencies
```

## Customer Discovery

We're actively talking to house flippers. If you're interested in trying FlipIQ or providing feedback:

### For Flippers
1. Check out the [landing page](landing_page.html)
2. Try the [live dashboard](#try-the-demo)
3. [Sign up for beta access](landing_page.html#signup)

### For Investors/Partners
See our comprehensive documentation:
- [`docs/investor_memo.md`](docs/investor_memo.md) — Investment opportunity
- [`docs/market_analysis.md`](docs/market_analysis.md) — $118B TAM
- [`docs/financial_projections.md`](docs/financial_projections.md) — 3-year model

---

## Dashboard Overview

| Tab | Description |
|-----|-------------|
| **Top Opportunities** | Ranked list of flip opportunities with composite scores |
| **Geographic View** | US choropleth map and state/metro analysis |
| **Score Analysis** | Score distributions, correlations, scatter plots |
| **Market Trends** | ZHVI time series and YoY appreciation charts |
| **Compare ZIPs** | Side-by-side ZIP code comparison with radar chart |
| **Agent Monitoring** | Agent status, alerts, timeline, decision logs, deep dive |

---

## Scoring Model

The 5-factor composite score (0-100) combines:

| Factor | Weight | Signal |
|--------|--------|--------|
| **Appreciation** | 25% | 12-month price growth (ZHVI) |
| **Velocity** | 25% | Days to pending sale (liquidity) |
| **Distress** | 20% | % of listings with price cuts |
| **Pricing Power** | 15% | Sale-to-list ratio |
| **Value Gap** | 15% | Bottom-tier vs all-homes spread |

### Strategy Presets

| Strategy | Best For |
|----------|----------|
| **Fast Flip** | Quick turns, high liquidity markets |
| **Value-Add** | Renovation opportunities, distressed sellers |
| **Balanced** | General-purpose scoring |

---

## Agent System

| Agent | Function |
|-------|----------|
| **DataRefreshAgent** | Monitors for new Zillow data releases |
| **ScoringAgent** | Computes opportunity scores for all ZIPs |
| **OpportunityDetectionAgent** | Identifies new/changed opportunities |
| **PropertyAnalysisAgent** | Performs deep-dive analysis |
| **AlertAgent** | Generates priority-based alerts |
| **ReportGeneratorAgent** | Creates weekly summary reports |

---

## Key Deliverables

### Technical MVP
- Fully functional scoring engine analyzing 26K+ ZIPs
- 6 autonomous agents with orchestration
- Interactive 6-tab dashboard
- Property analysis with investment recommendations

### Business Documentation
- Market analysis with $118B TAM sizing
- Unit economics (5.4:1 LTV:CAC)
- 3-year financial projections ($10.7M ARR)
- Comprehensive risk analysis (19 risks, 6 categories)

### Customer Validation Materials
- Landing page with signup form and ROI calculator
- Customer discovery templates and scripts
- Demo video script and presentation deck
- Use cases and competitive analysis

### Investor Materials
- 13-slide pitch deck content
- Confidential investment memorandum
- One-page executive summary

---

## Documentation Index

### Getting Started
- [`README.md`](README.md) — This file
- [`docs/DEMO.md`](docs/DEMO.md) — 5-minute demo walkthrough (IN PROGRESS)
- [`docs/architecture.md`](docs/architecture.md) — System architecture

### Customer Validation
- [`docs/CUSTOMER_VALIDATION.md`](docs/CUSTOMER_VALIDATION.md) — Validation strategy

### Demo & Sales
- [`docs/value_props/`](docs/value_props/) — Use cases, ROI, competitive analysis

### Business & Investment
- [`docs/market_analysis.md`](docs/market_analysis.md) — Market sizing
- [`docs/unit_economics.md`](docs/unit_economics.md) — LTV, CAC, pricing
- [`docs/financial_projections.md`](docs/financial_projections.md) — 3-year model
- [`docs/investor_memo.md`](docs/investor_memo.md) — Investment opportunity
- [`docs/risk_analysis.md`](docs/risk_analysis.md) — Risk assessment

---

## Future Roadmap

| Phase | Enhancement |
|-------|-------------|
| **Phase 1** | Customer validation (current) |
| **Phase 2** | Live Zillow API integration |
| **Phase 3** | MLS data for property-level analysis |
| **Phase 4** | User accounts, saved searches |
| **Phase 5** | Mobile app with push notifications |

---

## Important Notes

> **This is a validation-stage MVP** built to demonstrate the concept and gather customer feedback. The system uses historical Zillow Research data (2022-2025) and simulated agent runs (for now!).

> **Financial projections assume validation success.** Numbers in business documentation represent potential outcomes if product-market fit is achieved.

> For production deployment, the system would require:
> - Live data feeds (Zillow API, MLS, county records)
> - Database layer for multi-user support
> - Authentication and authorization
> - Scheduled job infrastructure (cron/Airflow)
> - Alert delivery system (email, SMS, push)

---

## Data Sources

- [Zillow Research Data](https://www.zillow.com/research/data/) — Public datasets
- ZHVI (Zillow Home Value Index) — ZIP, County, Metro levels
- Market indicators — Days to pending, price cuts, sale-to-list ratio

---

## Contact

**Abhay Puri** — [LinkedIn](https://linkedin.com/in/abhaypuri1)

**Anthony Nastasi** — [LinkedIn](https://www.linkedin.com/in/anthony-g-nastasi-b8a387143/)

---

## Interested in FlipIQ?

- **House Flippers:** [Sign up for beta access](landing_page.html)
- **Investors:** [Read the investment memo](docs/investor_memo.md)
- **Partners:** [Contact us](abhaypuri189@gmail.com)
