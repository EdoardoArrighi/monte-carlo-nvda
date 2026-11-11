# Monte Carlo Simulation of NVIDIA Stock Prices

A Python project that simulates possible future NVIDIA (NVDA) stock-price paths using historical market data and Geometric Brownian Motion (GBM).

> This project is for educational purposes only and does not constitute financial advice.

## Overview

The project:

- Downloads the previous five years of adjusted NVIDIA stock-price data;
- Calculates daily logarithmic returns;
- Estimates annualized return and volatility;
- Simulates 10,000 possible price paths over one year;
- Visualizes the simulated paths and the distribution of terminal prices.

## Methodology

The simulation uses the Geometric Brownian Motion (GBM) model.

For each trading day, the model combines:

- an expected return estimated from NVIDIA’s historical log-returns;
- volatility estimated from the same historical data;
- a random shock drawn from a standard normal distribution.

The model simulates price changes in exponential form. This ensures that simulated stock prices remain positive.

The simulation uses 252 trading days to represent one year.

## Results

The notebook produces:

1. A chart with 10,000 simulated NVIDIA price paths;
2. A red line representing the average simulated price;
3. A histogram of simulated terminal prices after one year.

The terminal-price distribution is positively skewed, which is consistent with the lognormal distribution produced by the GBM model.

## Installation

Install the required libraries:

```bash
pip install numpy pandas matplotlib yfinance
```

## Usage

1. Clone this repository:

```bash
git clone https://github.com/YOUR-USERNAME/monte-carlo-nvda.git
```

2. Open the notebook:

```text
Montecarlo_github_.ipynb
```

3. Run all cells from top to bottom.

The notebook downloads the latest available five-year NVDA price history when executed.

## Project Structure

```text
monte-carlo-nvda/
│
├── Montecarlo_github_.ipynb
├── README.md
├── LICENSE
└── .gitignore
```

## Disclaimer

Past market performance does not guarantee future results. The Monte Carlo simulation provides possible scenarios based on historical return and volatility; it is not a prediction of future NVIDIA prices.

## License

This project is distributed under the MIT License.
