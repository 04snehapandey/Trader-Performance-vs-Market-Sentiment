# Trader-Performance-vs-Market-Sentiment
 How market sentiment (Fear/Greed) relates to trader behavior and performance on Hyperliquid. 

📌 Overview
This project analyzes whether trader performance and behavior differ across market sentiment regimes (Fear vs Greed).
The analysis focuses on:
Performance metrics (Win rate, PnL, Drawdown proxy)
Behavioral changes (Trade frequency, Position size, Long/Short bias)
Trader segmentation (Frequent vs Infrequent, Consistent vs Volatile)
The objective is to determine if market sentiment materially impacts profitability and trading behavior, and to propose actionable strategy improvements.

📂 Dataset
The project uses two datasets:
Trades Dataset
Sentiment Dataset



Classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)
The datasets are merged by date after timestamp normalization.

⚙️ Setup Instructions
1️⃣ Clone Repository
git clone <repository-link>
cd <project-folder>

2️⃣ Create Virtual Environment (Optional but Recommended)
python -m venv venv
Activate environment:
Windows
venv\Scripts\activate
Mac/Linux
source venv/bin/activate

3️⃣ Install Dependencies
pip install pandas numpy matplotlib jupyter
Or install using:
pip install -r requirements.txt

▶️ How to Run
Option 1 — Jupyter Notebook (Recommended)
jupyter notebook
Open the  notebook and run all cells sequentially.

This will:
Clean and format timestamps
Merge sentiment with trade data
Compute performance metrics
Generate plots for analysis
Create trader segmentation

📊 Analysis Performed
🔹 Performance Analysis
Win Rate by Sentiment
Average PnL per Trade
Average Daily PnL
Drawdown Proxy (Worst Daily Loss)

🔹 Behavioral Analysis
Number of Trades by Sentiment
Average Trade Size
Long/Short Distribution

🔹 Trader Segmentation
Frequent vs Infrequent Traders
Consistent vs Volatile Traders
Large vs Small Position Traders

🔍 Key Findings
Win rate increases significantly during Extreme Greed compared to Extreme Fear.
Traders increase trade size and activity during bullish sentiment.
Volatile traders experience larger drawdowns during Fear periods.
Sentiment has measurable impact on both profitability and behavior.

💡 Strategy Recommendations
Sentiment-Adaptive Position Sizing
Increase exposure during Extreme Greed; reduce exposure during Extreme Fear.

Segment-Based Risk Control
Apply stricter controls to volatile traders during Fear phases while allowing disciplined traders to capitalize on bullish regimes.

🛠 Tech Stack

Python 
Pandas
Matplotlib
Jupyter Notebook

📌 Assumptions
Win defined as closed_pnl > 0
Sentiment merged on trade date
Daily PnL calculated per account
Drawdown proxy = worst daily PnL per sentiment regime
