This project analyzes how cryptocurrency trader behavior and performance change under different market sentiment regimes using the Bitcoin Fear & Greed Index.

The objective is to understand whether trader profitability, trading activity, and risk behavior vary during Fear and Greed market conditions, and to derive insights that may inform better trading strategies.

Objective

The main goal of this analysis is to explore the relationship between market sentiment and trader performance.

Specifically, this project aims to:

Compare trader performance across different sentiment regimes

Identify behavioral patterns such as trade size and trading frequency

Analyze trader consistency and risk-adjusted performance

Generate insights that could support smarter trading strategies

Datasets Used
1. Bitcoin Fear & Greed Index

This dataset provides daily market sentiment values.

Columns include:

date – sentiment date

value – sentiment score

classification – sentiment category (Fear, Greed, Extreme Fear, Extreme Greed)

2. Historical Trader Data (Hyperliquid)

This dataset contains historical trading records from the Hyperliquid platform.

Important fields include:

account – trader wallet address

coin – traded asset

execution_price – price at which the trade was executed

size_usd – value of the trade in USD

side – buy or sell direction

timestamp_ist – trade timestamp

closed_pnl – realized profit or loss from the trade

Methodology

The analysis follows a structured data science workflow:

1. Data Preparation

Load both datasets

Standardize column names

Convert timestamps into date format

Merge trading data with sentiment data

Handle missing values and check duplicates

2. Feature Engineering

Additional metrics were created for analysis:

profit indicator (is_profit)

trade size segmentation

daily trading activity

long vs short ratio

risk-adjusted trader performance

3. Exploratory Data Analysis

Several analyses were performed to evaluate trader performance:

Average PnL across sentiment regimes

Trade frequency during fear vs greed periods

Win rate of trades

Buy vs sell behavior

Trade size segmentation

Trader consistency analysis

Risk-adjusted performance evaluation

Visualizations

The notebook includes several charts to better understand trader behavior:

Trader PnL vs market sentiment

Average trade size by sentiment

Distribution of trader profits

Distribution of risk-adjusted performance

These visualizations help highlight how trader behavior changes across different sentiment regimes.

Key Insights

Trader profitability tends to be stronger during fear sentiment periods, suggesting traders may exploit market dips.

Trading activity increases during extreme sentiment conditions, indicating higher participation and risk-taking behavior.

Buy orders become more frequent during fear markets, reflecting dip-buying strategies.

Larger trades generate higher average profits but also introduce higher variability in outcomes.

A relatively small group of traders contributes a large share of total profits.

Risk-adjusted performance appears stronger during fear sentiment regimes, indicating better reward relative to risk.

Strategy Recommendations

Based on the analysis, the following strategy ideas emerge:

1. Opportunistic Trading During Fear

During fear sentiment periods, traders may consider increasing trade frequency or moderately increasing position sizes to capture potential rebound opportunities.

2. Risk Control During Greed

During greed sentiment periods, traders should reduce leverage exposure and apply stricter risk management since profitability becomes less consistent despite higher trading activity.

Technologies Used

This project was implemented using:

Python

Pandas

NumPy

Matplotlib

Seaborn

Jupyter Notebook

Repository Structure
primetrade-ai-data-science-internship
│
├── trader_analysis.ipynb
├── historical_data.csv
├── fear_greed_index.csv
└── README.md
Conclusion

This study highlights how trader behavior changes depending on market sentiment. Fear periods appear to offer stronger opportunities for profitable entries, while greed periods tend to increase trading activity but reduce consistency in returns.

Understanding these sentiment-driven patterns can help traders design strategies that adapt to changing market conditions.
