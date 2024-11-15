
---

# Stock Price Prediction Using Black-Scholes and Monte Carlo Models

This repository contains a Python implementation of stock price prediction for Apple Inc. (AAPL) using **Black-Scholes**, **Monte Carlo**, and **Advanced Monte Carlo** models. The project demonstrates the pricing of call and put options, employing simulation-based approaches alongside the analytical Black-Scholes model.

---

## Features

1. **Historical Data Analysis**:
   - Retrieves and visualizes historical stock prices using `yfinance` and `matplotlib`.

2. **Option Pricing Models**:
   - **Black-Scholes Model**: Analytical pricing for European call and put options.
   - **Monte Carlo Simulation**: Numerical simulation for option pricing.
   - **Antithetic Variance Reduction in Monte Carlo**: Enhances simulation efficiency by reducing variance.

3. **Parameter Inputs**:
   - Spot price, strike price, risk-free rate, volatility, time to maturity, number of simulations, and time steps.

4. **Performance Comparison**:
   - Results from each model are compared to demonstrate differences in accuracy and efficiency.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/stock-price-prediction.git
   cd stock-price-prediction
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. (Optional) Install `yfinance` if not already installed:
   ```bash
   pip install yfinance
   ```

---

## Models Overview

### 1. Black-Scholes Model
   - Provides a closed-form solution for European option pricing.
   - Requires inputs: stock price, strike price, risk-free rate, volatility, and time to maturity.
   - Outputs the call and put option prices.

### 2. Monte Carlo Simulation
   - Simulates thousands of possible future stock price paths using a random walk approach.
   - Estimates option prices by averaging discounted payoffs.
   - Parameters: number of simulations and time steps.

### 3. Antithetic Monte Carlo Simulation
   - Uses antithetic variates to reduce variance in Monte Carlo simulations.
   - Improves accuracy and convergence speed.

---

## How to Use

1. **Fetch Historical Data**:
   - Adjust the ticker symbol and time period to retrieve stock price data:
     ```python
     ticker_data = yf.Ticker('AAPL')
     historical_data = ticker_data.history(period="5y")
     ```

2. **Run Models**:
   - Modify parameters as needed (e.g., spot price, strike price, etc.).
   - Execute the code cells to calculate option prices using each model.

3. **Visualize Results**:
   - Generate stock price charts and compare model outputs.

---

## Sample Output

### Parameters:
- Spot Price: $100
- Strike Price: $100
- Risk-Free Rate: 5%
- Volatility: 20%
- Time to Maturity: 1 year
- Simulations: 10,000
- Steps: 100

### Results:
| Model                    | Call Price | Put Price |
|---------------------------|------------|-----------|
| Black-Scholes            | 10.45      | 5.75      |
| Monte Carlo              | 10.25      | 5.55      |
| Antithetic Monte Carlo   | 10.35      | 5.58      |

---
