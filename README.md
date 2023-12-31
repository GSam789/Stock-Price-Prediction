# Stock-Price-Prediction

## Project Overview:
### Objective:
The primary goal was to empower investors with more informed strategies by creating a tool that simplifies decision-making through the analysis of stock data and sentiment from financial news articles.

### Data Collection and Cleaning:
- **Stock Data:** Utilized Yahoo Finance's API to gather comprehensive stock data for Amazon, Apple, and Microsoft from October 1, 2018, to September 30, 2023.
- **News Sentiment Data:** Performed sentiment analysis on financial news articles using VADER and TextBlob. Cleaned the resulting data, including article details and sentiment scores, by removing redundancies and duplicates.

### Methodology:

#### 1. Sentiment Analysis:

- Leveraged VADER and TextBlob to generate sentiment scores for financial news data.
- Aggregated sentiment scores for different trading days to capture overall sentiment.
- Integrated sentiment scores with historical stock data to predict next-day Adjusted Close prices.

#### 2. LSTM Model:

- Created input sequences and output values for training the LSTM model.
- Implemented a three-layer LSTM model with 200 units, Dense layer with 50 units, and an output Dense layer with 3 output units.
- Used Adam optimizer, Mean Squared Error (MSE) loss function, and monitored Mean Absolute Error (MAE) and Mean Absolute Percentage Error (MAPE) during training.

#### 3. Transformer Model:

- Defined a transformer block capturing complex dependencies in sequential data.
- Built a transformer model by stacking multiple transformer blocks.
- Applied Global Average Pooling and added a Multi-Layer Perceptron (MLP) head.
- Compiled the model using MSE loss function, Adam optimizer, and metrics like MAE and MAPE for evaluation.

### Results and Challenges:
The Transformer model consistently outperformed the LSTM model across all three stocks for various error metrics.
The project faced challenges during the merging of stock and sentiment data, leading to a substantial decrease in the dataset.

### Lessons Learned:
The importance of data preprocessing and cleaning for a robust analysis.
Understanding the limitations of models and their sensitivity to data quality and quantity.
Recognizing the potential of transformer models in handling sequential data with long-range dependencies.
