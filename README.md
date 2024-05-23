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
