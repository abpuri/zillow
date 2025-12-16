# House Flipper Property Identification Agent

Automated workflow to identify undervalued properties for house flipping using Zillow Research data.

## Data Sources
- Zillow Research Public Data (https://www.zillow.com/research/data/)
- Last updated: December 2025
- Coverage: 2022-2025 (3 years)

## Datasets
1. **ZHVI All Homes (ZIP)** - Home value trends by ZIP code
2. **ZHVI Bottom-Tier (County)** - Undervalued segment analysis  
3. **Days to Pending (Metro)** - Market velocity
4. **Price Cuts (Metro)** - Seller distress indicator
5. **Sale-to-List Ratio (Metro)** - Pricing power
6. **Market Heat Index (Metro)** - Supply/demand composite

## Project Structure
```
zillow/
├── data/
│   ├── raw/zillow/       # Original Zillow CSVs
│   └── processed/        # Cleaned/transformed data
├── notebooks/            # EDA and analysis
├── src/                  # Core modules
└── requirements.txt
```

## Setup
```bash
pip install -r requirements.txt
```
