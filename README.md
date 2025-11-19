# Stock Market Clustering Analysis

![Stock Market](https://img.shields.io/badge/Stock%20Market-Clustering-blue) ![Apache Kafka](https://img.shields.io/badge/Apache-Kafka-red) ![PySpark](https://img.shields.io/badge/Apache-PySpark-orange) ![ML](https://img.shields.io/badge/Machine-Learning-brightgreen)

## Project Overview

This project implements an advanced data pipeline for analyzing and clustering stock market data using Big Data technologies. The system leverages **Apache Kafka** for real-time data streaming and **Apache Spark** for distributed computing and machine learning.

### Key Features

- **Real-time Data Collection**: Fetches stock market data from Yahoo Finance API
- **Data Streaming**: Implements Apache Kafka for efficient data streaming
- **Distributed Processing**: Uses PySpark for scalable data processing
- **Machine Learning**: Applies K-means clustering to identify stock behavior patterns
- **Visualization**: Includes correlation heatmaps, 3D cluster visualization, and PCA-based analysis

## Technologies Used

- **Apache Kafka**: Real-time data streaming platform
- **Apache Spark**: Distributed computing framework
- **PySpark ML**: Machine learning library for Spark
- **Yahoo Finance API**: Stock market data source
- **Matplotlib & Seaborn**: Data visualization
- **TA-Lib**: Technical analysis library
- **Jupyter Notebook**: Interactive development environment

## Architecture

The project follows a comprehensive data pipeline architecture:

1. **Data Collection Layer**: Yahoo Finance API fetches historical stock data
2. **Streaming Layer**: Apache Kafka handles data streaming with topic creation for each stock
3. **Processing Layer**: PySpark processes and transforms the data
4. **Analysis Layer**: ML algorithms (K-means) identify stock clusters
5. **Visualization Layer**: Various plotting techniques present insights

## Implementation Details

### Data Collection

The system collects 6 months of historical data (April-September 2023) for 50+ major stocks including AAPL, GOOGL, MSFT, TSLA, and others. Data attributes include:

- Open, High, Low, Close prices
- Trading Volume

### Kafka Integration

- Creates individual topics for each stock ticker
- Efficiently streams price and volume data
- Ensures data integrity and system reliability

### Cluster Analysis

The project determines the optimal number of clusters through multiple evaluation techniques:

- **Silhouette Score**: Measures cluster separation quality
- **Elbow Method**: Identifies the point of diminishing returns for additional clusters
- **PCA Visualization**: Visual representation of cluster separation

Based on comprehensive evaluation, **K=4** was selected as the optimal cluster count.

## Results and Insights

The clustering analysis identified four distinct stock behavior patterns, which can be utilized for:

1. **Portfolio Diversification**: Select stocks from different clusters to reduce overall risk
2. **Market Segmentation**: Understand different segments of market behavior
3. **Trading Strategy Development**: Develop specific strategies for each cluster
4. **Risk Management**: Identify higher volatility clusters

## How to Run the Project

1. **Clone the repository**:
   ```
   git clone https://github.com/yourusername/stock-clustering-analysis.git
   ```

2. **Install dependencies**:
   ```
   pip install -r requirements.txt
   ```

3. **Download and setup Apache Kafka**:
   The notebook includes commands to download and setup Kafka automatically.

4. **Run the Jupyter Notebook**:
   ```
   jupyter notebook "Stock Clustering Analysis.ipynb"
   ```

## Future Work

Potential enhancements for this project include:

- Integration with real-time stock data feeds
- Implementation of sentiment analysis from financial news
- Exploration of alternative clustering algorithms (DBSCAN, hierarchical)
- Development of predictive models based on cluster insights
- Extended time-series analysis for long-term pattern recognition

## Contributors

- Seyyed Alireza Khoshsolat
- Farshad Farahtaj

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- University of Naples Federico II
- Prof. Giancarlo Sperli for project supervision
- Yahoo Finance API for providing financial data
