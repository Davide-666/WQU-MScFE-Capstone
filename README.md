##### (work in progress)
# WQU-MScFE-Capstone
# Hybrid Deep Learning for Portfolio Allocation
### Student Group 11196
### * Davide Freni	davide.freni@gmail.com 
### * Vicky Singh	ivickysingh@yahoo.com
### * Kenneth Kariuki	kenkarish1935@gmail.com

This repository contains the material developed for my Capstone Project in the Master of Science in Financial Engineering program at WorldQuant University. The study explores how newer tools from machine learning and deep learning can be applied to portfolio construction. The central aim is to build an approach that is transparent and robust, while still practical for trading portfolios of liquid assets.

## Project Overview
The field of portfolio allocation owes much to Harry Markowitz, whose Modern Portfolio Theory in the 1950s gave finance its first structured way to think about diversification and risk. Later, the Black–Litterman model tried to make the approach more stable by incorporating investor views. These frameworks still dominate textbooks and courses. But their limitations are clear: estimates are noisy, correlations often spike during crises, and the assumption of normal returns rarely matches market behavior.

Over time, industry practice has moved in several directions. Robo-advisors grew quickly by making investing easy and cheap, although their models remain fairly rigid. Hedge funds went the other way, developing highly advanced proprietary systems, though these are kept strictly confidential. More recently, open-source projects experimenting with reinforcement learning have generated excitement, but many of these prototypes fail to cope when tested against real market conditions.

This project takes a blended approach. Three techniques form the backbone of the framework:
* Long Short-Term Memory networks (LSTMs) are used to pick up sequential patterns in returns.
* Gradient Boosting (XGBoost) sharpens cross-sectional predictions.
* Reinforcement Learning (RL) allows allocations to shift dynamically as new data comes in.

From the outset, the design placed a strong emphasis on robustness. Liquidity filters, stress scenarios, and Monte Carlo simulations are built directly into the framework. The intention is not simply to show appealing backtests, but to test whether such a system could survive the demands of actual trading.

## Academic Contribution
The project makes three contributions worth highlighting. First, it demonstrates how several machine learning methods can be integrated into a single portfolio allocation system, bridging a gap between the academic focus on isolated models and the multifaceted challenges of practice. Second, it treats robustness as a central concern rather than an afterthought, by weaving stress tests, liquidity constraints, and extreme-scenario analysis into the evaluation. Finally, it is made reproducible: the methods are documented and can be replicated, which makes the work accessible to academics and potentially useful for fintech practitioners.

## Repository Contents
The repository has been arranged to make the workflow clear:
* data/: sample financial datasets prepared for confidentiality.
* notebooks/: exploratory notebooks with experiments and figures.
* src/: source code for data processing, model training, backtesting, and stress testing.
* reports/: the written Capstone report with comparative analysis and references.
* results/: model performance outputs and visualizations.

## Results in Brief
Out-of-sample tests indicate that the hybrid framework can outperform classical mean–variance optimization during volatile periods. It also showed more stability under simulated stress than simple robo-advisory benchmarks. By focusing only on highly liquid assets, the framework avoids many of the execution problems—such as slippage—that often undermine academic strategies.

Taken together, the findings suggest that predictive accuracy and robustness can be combined effectively. The framework is both a research contribution and a model with the potential to be applied in practice.

### References (selected)
Markowitz, Harry. “Portfolio Selection.” The Journal of Finance, 1952.

Black, Fischer, and Robert Litterman. “Global Portfolio Optimization.” Financial Analysts Journal, 1992.

Breiman, Leo. “Random Forests.” Machine Learning, 2001.

Chen, Tianqi, and Carlos Guestrin. “XGBoost: A Scalable Tree Boosting System.” KDD Conference Proceedings, 2016.

Hochreiter, Sepp, and Jürgen Schmidhuber. “Long Short-Term Memory.” Neural Computation, 1997.

Moody, John, and Matthew Saffell. “Learning to Trade via Direct Reinforcement.” IEEE Transactions on Neural Networks, 2001.

### License
This repository is provided for academic and research purposes. Please acknowledge the work if you make use of it in your own research or teaching.
