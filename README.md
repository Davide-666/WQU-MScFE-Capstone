# Beyond Markowitz: An Institutional Analysis of AI-Driven Portfolio Optimization 

This repository contains the material developed for the Capstone Project in the Master of Science in Financial Engineering program at WorldQuant University,
e.g the code and documentation for **Smartportfolios**, a new framework for quantitative portfolio allocation that combines traditional finance models with state-of-the-art techniques from **Machine Learning (ML)**, **Deep Learning (DL)**, and **Reinforcement Learning (RL)**.

The project evaluates and compares the performance of five distinct portfolio management strategies on market data from **2023–2024**.

***

## Project Overview

[cite_start]Traditional portfolio optimization methods, such as **Markowitz Mean-Variance Optimization (MVO)**, often struggle due to their sensitivity to input errors and their inability to adapt to non-linear market dynamics. This project addresses these limitations by implementing and backtesting adaptive, data-driven strategies.

### Novel Contributions
1.  **Reinforcement Learning (PPO) Strategy**: Implementation of a **Proximal Policy Optimization (PPO)** agent to learn dynamic, risk-adjusted asset allocation policies
2.  **Dynamic Switching Hybrid Ensemble**: A robust ensemble model that dynamically switches between the predictions of multiple models based on changing market conditions.

***

## Strategies Implemented

The project compares the performance of the following six strategies:

| Strategy Category | Model Name | Description |
| :--- | :--- | :--- |
| **Traditional** | **Markowitz (Mean-Variance)** | Classical optimization aiming to maximize return for a given level of risk. |
| **Machine Learning** | **Random Forest** | Uses Random Forest Regression to predict future returns, which are then used for optimization. |
| **Deep Learning** | **Simple Neural Network** | A basic Neural Network model to predict returns and determine portfolio weights. |
| **Reinforcement Learning** | **PPO-Agent** | An agent trained with the **Proximal Policy Optimization** algorithm to maximize cumulative reward (return). |
| **Hybrid** | **Dynamic Ensemble** | A strategy that combines the predictions of Markowitz, ML, DL, and RL, dynamically allocating weights based on market regime. |
| **Baseline** | **Equal Weight (1/N)** | A simple strategy where assets are equally weighted, serving as a robust benchmark. |

***

## Key Findings

The comparison of the five strategies revealed that AI-driven methods and the simple Equal Weight strategy significantly outperformed traditional optimization models on the 2023–2024 data.

| Strategy | Total Return | CAGR | Volatility | Sharpe Ratio | Max Drawdown |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **RRL (PPO)** | **524.92%** | **47.31%** | 27.99% | **1.69** | **-42.68%** |
| Equal Weight | 524.58% | 47.3% | 27.99% | 1.69 | -42.72% |
| Random Forest | 519.64% | 47.05% | 27.98% | 1.68 | -42.65% |
| Hybrid Ensemble | 502.93% | 46.2% | 28.69% | 1.61 | -45.75% |
| Markowitz | 428.9% | 42.2% | **34.52%** | **1.22** | **-57.97%** |
[cite: 45]

* **Top Performer**: The **Reinforcement Learning (PPO) strategy** delivered the highest return and the best risk-adjusted performance (Sharpe Ratio).
* **Traditional Underperformance**: The **Traditional Markowitz model** significantly underperformed and was the loser, exhibiting the highest volatility and maximum drawdown risk (-57.97%).
* **Risk Mitigation**: The AI models successfully minimized drawdowns (to ~43% vs 58% for Markowitz) by prioritizing **Risk Management** and "learning" that broad diversification was safer than concentration.

***

## Repository Structure & How to Run

The main deliverable is contained within a single executable notebook.

### File Structure

* `M7 - Final_project.ipynb`: The core code, including data fetching, model implementations (Markowitz, ML, DL, PPO, Ensemble), backtesting, and visualization logic.
* `M7 - Final report.pdf`: The full academic report detailing the methodology, theoretical framework, and results.
* `M7 - Solution Design Document.pdf`: The architectural overview and design choices for the project.

### Prerequisites

The project is built using **Python 3.8+**. Key dependencies include:

| Library | Purpose |
| :--- | :--- |
| `pandas`, `numpy` | Data manipulation and numerical operations. |
| `yfinance` | Downloading historical market data. |
| `scikit-learn` | Machine Learning models (Random Forest, etc.). |
| `scipy.optimize` | Traditional Mean-Variance Optimization. |
| `stable-baselines3` (Implied) | Reinforcement Learning PPO Agent. |
| `matplotlib`, `seaborn`, `plotly` | Data visualization and performance charting. |

### Execution

1.  **Clone the repository.**
2.  **Install dependencies** (e.g., install libraries like `yfinance`, `scikit-learn`, `stable-baselines3`).
3.  **Run the Jupyter Notebook**: Open `final_project.ipynb` and execute all cells sequentially. The notebook handles data download (2023-2024), model training, walk-forward backtesting, and result generation.

***

## Future Scope of Work

Potential extensions to the project include:

* **Introduce Real-World Frictions**: Integrate realistic transaction fees, slippage, and market impact into the backtesting model.
* **Expand Data Horizons**: Extend the backtesting period and the asset universe, along with implementing stronger backtesting methodologies.
* **Integrate Real-Time ESG Data**: Incorporate dynamic Environmental, Social, and Governance (ESG) data instead of mock scores.
* **Further Develop the Hybrid Ensemble**: Enhance the dynamic switching logic and robustness of the "Hybrid Ensemble" approach.

***

## Authors & Contact
* **Student Group 11196**
* **Vicky Singh** - ivickysingh@yahoo.com
* **Davide Freni** - davide.freni@gmail.com (Also responsible for **full management of the GitHub project repository** 
* **Kenneth Kariuki** - kenkarish1935@gmail.com

**Project Repository**: <https://github.com/Davide-666/WQU-MScFE-Capstone> 

