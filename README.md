# Financial ML
The raw, unprocessed dataset is usually the starting point of every significant discovery in quant world. So it is important to understand strict categorical differences financial data has within itself, as the approaches and discovery opportunities greatly differ across the mentioned categories.
- The document provides an overview of essential financial data types and their characteristics.
- Emphasis is placed on the accessibility, latency, and potential value of different data types for financial analysis and strategy research.

## Fundamental Data
1. **Characteristics**:
   - **Very low latency**: Data is updated and accessible in real-time or near-real-time.
   - **Easily accessible**: Widely available to financial analysts and institutions.
   - **Unlikely to find unexploited value**: Due to its accessibility, opportunities for unique insights may be limited.
   - **Usefulness**: Despite limited unique insights, fundamental data can still be valuable for analysis.

2. **Types**:
   - **FIX messages**: Financial Information Exchange messages, a protocol for real-time exchange of information.
   - **BWIC (Bids Wanted in Competition)**: Used in bond markets for sellers seeking bids.
   - **Challenges**: Fundamental data can be harder to process due to its volume and complexity, but it offers rich potential for strategy development.

## Market Data
1. **Variety**:
   - Financial data varies widely in form and source.
   - It can originate from an original source or be processed for enhanced utility.

2. **Enhancements**:
   - **Features/Data Creation**: Data can be transformed into features or new data points to improve financial models.
   - **Sentiment Signals**: Derived from news, social media, and other textual sources to gauge market sentiment.
   - **Strategy Signals**: Indicators or patterns identified to inform trading strategies.

## Analytics
1. **Nature**:
   - The diversity of data increases from fundamental to alternative data.
   - Analytics data is often unique, difficult to process, and store.

2. **Sources**:
   - **Produced by**: Individuals, business processes, and various sensors.
   - This category includes diverse and often complex data sets that require sophisticated processing techniques.

## Alternative Data
1. **Characteristics**:
   - **Truly unique**: Often not widely available or utilized, providing opportunities for unique insights.
   - **Hard-to-process and store**: Due to the complexity and volume of the data.
   - **Produced by**: Various sources including individuals, business operations, and physical sensors.


- Financial data can be categorized into fundamental, market, analytics, and alternative data, each with its own characteristics and challenges.
- While fundamental and market data are more accessible and widely used, analytics and alternative data offer unique opportunities for insights but require advanced processing capabilities.
- Understanding the nuances of each data type can aid in developing robust financial strategies and models.




## Why Data Bars?

**Purpose**:
- **Machine Learning on Unstructured Data**: To utilize machine learning (ML) algorithms effectively, it is crucial to transform unstructured data into a structured format.
- **Regularized Format**: This transformation involves parsing the data, extracting valuable information, and storing it in a consistent and structured manner.

**Key Information Collected**:
1. **Timestamp**: The specific time at which data is recorded.
2. **Volume-weighted average price (VWAP)**: A trading benchmark calculated by dividing the total dollar value traded by the total volume traded over a particular time period.
3. **Open Price**: The first price at which a security is traded at the beginning of the trading session.
4. **Close Price**: The last price at which a security is traded at the end of the trading session.
5. **High Price**: The highest price at which a security is traded during a specific time period.
6. **Low Price**: The lowest price at which a security is traded during a specific time period.
7. **Volume Traded**: The total number of shares or contracts traded for a security during a specified time period.

**Terminology**:
- **Bars**: In finance, the rows of extracted, structured, and ordered data are referred to as "bars." Each bar represents a summarized form of the data over a specified time period, such as a minute, hour, or day.

**Significance**:
- **Standardized Data Representation**: Bars help in standardizing the representation of financial data, making it easier to apply various analytical and ML techniques.
- **Enhanced Data Analysis**: By structuring data into bars, researchers and analysts can perform more precise and insightful analyses, leading to better decision-making in financial contexts.

- **Data bars** are essential for converting unstructured financial data into a structured format suitable for machine learning.
- They capture critical trading metrics such as timestamp, VWAP, open, close, high, low prices, and volume traded.
- This structured representation, known as "bars," is fundamental in financial data analysis and algorithmic trading.


## Overview of Data Bars

**Types of Data Bars**:
1. **Time Bars**: Sampled at fixed time intervals (e.g., every 5 minutes).
2. **Tick Bars**: Sampled based on a predefined number of transactions (e.g., every 5,000 ticks).
3. **Volume Bars**: Sampled when a predefined number of units have been traded (e.g., every 5,000 units).
4. **Dollar Bars**: Sampled when a predefined market value has been exchanged (e.g., every $5,000).
5. **Imbalance Bars**: Sampled based on the imbalance in certain indices.
6. **Run Bars**: Sampled more frequently when the sequence of buys diverges from expectations.

## Detailed Insights

**Time Bars**:
- Widely used but can exhibit poor statistical properties like serial correlation, heteroscedasticity, and non-normality of returns.
- Not recommended by some experts, including Marcos Lopez de Prado, due to these drawbacks.

**Tick Bars**:
- Provide samples each time a set number of transactions occur, better capturing market activity.
- Can achieve returns closer to independent and identically distributed (IID) values but are sensitive to outliers from auction trades at market open/close.

**Volume Bars**:
- Sampled every time a set number of units are traded, offering better statistical properties (closer to IID Gaussian distribution).
- Adjusted dynamically to remain robust against changes in the number of outstanding shares.

**Dollar Bars**:
- Based on the value exchanged, providing an unbiased view of price fluctuations.
- Often considered to have the best performance and recommended for frequent sampling.

**Imbalance Bars**:
- **Tick Imbalance Bars (TIBs)**: Sample when tick imbalances exceed expectations, treating each trade equally regardless of volume or price.
- **Dollar/Volume Imbalance Bars**: Extend TIBs to consider volumes and dollars, syncing sampling with informed traders’ activity.

**Run Bars**:
- **Tick Run Bars**: Focus on sequences of buys, sampling more when these sequences diverge from expectations.
- **Dollar/Volume Run Bars**: Extend the concept of run bars to volumes and dollars, tracking large traders’ activities.

## Analytical and Practical Insights

- **Dollar Bars**: Recommended for their superior performance.
- **Sampling Guidelines**: Aim for around 50 dollar bar samples per day.
- **Cost Reduction**: Using 1-minute data can substitute for tick data, reducing financial and computational costs.

## Handling Special Cases

- **ETF Trick**: Treats a basket of securities as a single cash product to avoid structural breaks from irregular payouts.
- **Single Future Roll**: Adjusts for cumulative roll gaps in futures data.
- **PCA Weights**: Allocates risks across principal components of the covariance matrix.

## Conclusion

- **Unstructured Data**: Essential for substantial discoveries in financial research.
- **Structured Data**: Creating robust and informative datasets through structured data (bars) is crucial for successful research.
- **Method to Chaos**: Using data structures effectively transforms chaotic raw data into valuable, structured insights.
