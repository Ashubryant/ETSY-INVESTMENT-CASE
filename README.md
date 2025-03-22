# Discounted Cash Flow (DCF) Valuation

## Project Overview
This project implements a Discounted Cash Flow (DCF) valuation model using Python. The goal is to estimate the intrinsic value of a stock based on its expected future cash flows. The project specifically fetches financial data for Etsy (ETSY) and applies DCF valuation techniques.

## Features
- Fetch financial data using `yfinance`
- Extract balance sheet, cash flow, and financial statements
- Implement DCF valuation model
- Calculate intrinsic value based on free cash flows and discounting techniques

## Installation
Ensure you have the following dependencies installed:
```sh
pip install yfinance pandas
import yfinance as yf
import pandas as pd

# Download financial data for Etsy (ETSY)
ticker = "ETSY"
stock = yf.Ticker(ticker)
financials = stock.financials
cash_flow = stock.cashflow
balance_sheet = stock.balance_sheet

print(financials)
# ETSY-INVESTMENT-CASE
def dcf_valuation(fcf, growth_rate, discount_rate, terminal_growth_rate):
    """
    Perform DCF valuation.
    :param fcf: List of free cash flows for the next 5 years.
    :param growth_rate: Assumed growth rate for FCF.
    :param discount_rate: Discount rate for NPV calculation.
    :param terminal_growth_rate: Long-term growth rate for terminal value.
    """
