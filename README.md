# Bid/Ask Spread Adjusted Carry Analyzer

## Purpose

This project explores how bid/ask spreads impact the realized economics of fixed-income carry trades over time.

Traditional carry calculations often assume execution at a theoretical market price. In practice, market participants must transact at either the bid or ask, introducing execution costs that can materially affect realized returns, particularly over shorter holding periods.

The objective of this model is to quantify the interaction between:

* Carry generation
* Financing costs
* Execution costs
* Holding period duration
* Dealer spread capture

and visualize how these factors evolve through time.

---

## Educational Objective

This project is intended as an educational tool for students interested in:

* Fixed Income Markets
* Treasury Financing
* Repo Markets
* Market Microstructure
* Relative Value Trading
* Dealer Economics
* Carry Trades

The model demonstrates how theoretical returns may differ from executable returns once transaction costs are considered.

---

## Inputs

The model allows the user to specify:

* Dirty Price
* Bid Price
* Ask Price
* Asset Yield
* Repo Rate
* Additional Funding Costs
* Holding Period (Days)
* Bid Size
* Ask Size

These inputs are used to calculate the expected value of carry generated under different execution assumptions.

---

## Methodology

The model applies continuously compounded carry using an exponential growth framework.

The future value of the position is estimated using:

```text
Future Value = Price × e^((Yield − Repo − Additional Costs) × Time)
```

Carry is calculated independently using:

* Bid Price
* Mid Price
* Ask Price

allowing direct comparison of execution outcomes.

---

## Outputs

The model generates:

* Carry at Bid
* Carry at Mid
* Carry at Ask
* Spread-Adjusted Carry
* Execution Cost Impact
* Dealer Premium Estimates
* Holding Period Sensitivity Analysis

The resulting calculations can be visualized across multiple holding periods to observe how execution costs influence financing returns through time.

---

## Key Insight

Execution costs are incurred immediately, while carry accrues gradually through time.

As a result:

* Short holding periods may experience significant spread drag.
* Longer holding periods may amortize execution costs.
* Realized carry can differ substantially from theoretical carry.

The model provides a framework for examining the relationship between financing returns and market microstructure.

---

## Disclaimer

This project is intended solely for educational and research purposes.

It is not investment advice, trading advice, or a recommendation to engage in any specific strategy. Calculations are simplified representations designed to illustrate financing and execution concepts within fixed-income markets.
