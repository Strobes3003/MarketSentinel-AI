# MarketSentinel-AI
Explainable Market Anomaly Detection for Early-Warning Surveillance

MarketSentinel AI is an AI-powered market surveillance prototype that analyzes historical stock-market data to identify unusual price and trading-volume patterns that may warrant further investigation.

The project combines financial time-series analysis, machine learning, anomaly scoring, and explainable alerts to help analysts investigate unusual market activity. The longer-term goal is to explore edge deployment and real-time visual monitoring using NVIDIA-powered AI pipelines.

Important: MarketSentinel identifies potentially suspicious patterns. Its alerts do not establish insider trading, market manipulation, or wrongdoing.

Problem Statement

Unusual price movements and trading-volume spikes can make it difficult to identify potentially suspicious market activity across large amounts of financial data. Simple threshold-based alerts may generate false positives, while unexplained model predictions provide limited investigative value.

MarketSentinel aims to detect unusual market behavior, quantify the associated risk signals, and present interpretable evidence for further analysis.

Objectives

Analyze historical stock-price and trading-volume data.

Engineer features that capture price behavior, volatility, and volume anomalies.

Compare Logistic Regression and Long Short-Term Memory (LSTM) models.

Identify and rank potentially suspicious time windows.

Explain alerts using the financial signals that contributed to them.

Evaluate detection performance on temporally separated datasets.

Investigate suitable NVIDIA edge-AI deployment workflows through PipeGen.

Proposed System Architecture

Historical Stock Market Data
            |
            v
Data Cleaning and Preprocessing
            |
            v
Financial Feature Engineering
            |
            v
Time-Window Construction
            |
            v
Machine Learning Models
  Logistic Regression / LSTM
            |
            v
Anomaly Detection and Risk Scoring
            |
            v
Explainable Alerts and Visualization
            |
            v
Evaluation and Analyst Review

PipeGen integration is a planned extension and will be included only if a suitable vision-based component can be implemented and validated against the hackathon's requirements.

Current Implementation

The supplied notebook provides the initial machine-learning workflow:

Historical OHLCV data retrieval using Yahoo Finance.

Feature engineering on stock-price and trading-volume data.

Construction of 10-day time windows.

Time-based training, validation, and testing splits.

Logistic Regression and LSTM model experiments.

The notebook's suspicious-window labels are generated using price-movement thresholds. Consequently, the current models primarily learn threshold-derived anomaly patterns rather than verified cases of market manipulation.

Planned Enhancements

Multi-signal anomaly detection: Combine abnormal returns, volume surges, and volatility changes.

Explainable alerts: Display the signals behind each alert instead of returning only a binary label.

Risk ranking: Prioritize unusual windows for analyst review.

Stronger evaluation: Report precision, recall, F1-score, false-positive rate, and performance on unseen future periods.

Visualization dashboard: Display stock charts, flagged windows, anomaly scores, and supporting evidence.

PipeGen feasibility and deployment: Validate a meaningful vision-pipeline use case and demonstrate the required compilation and execution workflow if supported by the chosen design.

These enhancements are planned and should not be considered completed until implemented and tested.

Technology Stack

Component

Technology

Programming language

Python

Data source

Yahoo Finance

Data processing

Pandas, NumPy

Machine learning

Scikit-learn

Deep learning

TensorFlow/Keras, if used by the notebook

Visualization

Matplotlib and/or Plotly

Development

Jupyter Notebook

Edge-AI exploration

NVIDIA GPU and CraftifAI PipeGen

The final dependency list will be determined by the implemented code and deployment environment.

Evaluation Methodology

The models will be compared using temporally separated datasets to reduce information leakage from future observations.

Evaluation metrics will include:

Precision

Recall

F1-score

False-positive rate

Inference latency

Where reliable, independently verified manipulation labels are unavailable, results will be described as detection of unusual market patterns rather than proven manipulation detection.

Expected Outcome

MarketSentinel aims to provide a prototype that identifies unusual stock-market behavior, explains the relevant signals, and helps prioritize periods for human investigation.

The project is intended for research and educational use. It is not a substitute for regulatory investigation, financial advice, or a verified market-abuse detection system.

Getting Started

Clone the repository.

Install the Python dependencies required by the notebook.

Open the notebook in Jupyter.

Run the data retrieval, preprocessing, feature engineering, and model evaluation cells.

Review the generated metrics and flagged time windows.

Exact setup commands and dependency versions will be added after the notebook has been tested in a clean environment.

Project Status

Stage: Initial machine-learning prototype with proposed explainability, dashboard, and edge-deployment extensions.

The financial anomaly-detection workflow is the starting point. PipeGen integration and real-time deployment remain subject to implementation and hackathon-track validation.

Disclaimer

MarketSentinel is an experimental analytical tool. Anomalies can arise from legitimate news, market volatility, liquidity changes, or other factors. A model prediction alone cannot establish manipulation or insider trading.

MarketSentinel AI — Detect unusual patterns. Explain the evidence. Support better investigations.

