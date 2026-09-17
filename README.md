# -econ3916-lab01-data-portfolio
# The Data Portfolio — Big Mac Index Analysis

## Objective

This project applies core data structuring and quality diagnostic techniques to The Economist's Big Mac Index, using purchasing power parity as a lens for evaluating global currency valuation.

## Methodology

- Loaded the Big Mac Index dataset directly from The Economist's public GitHub repository, spanning 57 countries and 45 time periods from April 2000 to July 2026, with 54 countries represented in the July 2024 cross-section
- Decomposed the panel dataset into its three constituent data structures — cross-sectional, time series, and panel — to illustrate how the same underlying data supports different analytical questions
- Computed implied Purchasing Power Parity exchange rates for each country by benchmarking local Big Mac prices against the U.S. dollar price, then derived a valuation percentage measuring deviation from PPP-implied exchange rates
- Conducted a systematic missing data audit, distinguishing between countries that exited the index, joined late, or experienced gaps mid-series, and classified the underlying mechanism (MCAR, MAR, or MNAR) for each pattern observed
- Built two visualizations: a horizontal bar chart ranking currency valuations for a single cross-section, and a multi-country time series tracking valuation trends over multiple decades

## Key Findings

- The Swiss franc has been persistently and substantially overvalued relative to the U.S. dollar, sitting at +41.8% above PPP-implied fair value in the July 2024 cross-section — a pattern consistent with high domestic labor, rent, and tax costs embedded in non-tradeable inputs
- The Japanese yen has trended undervalued on average across every decade covered by the dataset, suggesting a structurally different pricing dynamic relative to Switzerland
- Missing data in the panel is not random: Russia's exit reflects a clear MNAR mechanism tied to geopolitical sanctions rather than incidental non-response, underscoring that naive listwise deletion of incomplete countries would bias any cross-country PPP average toward more economically stable regimes
