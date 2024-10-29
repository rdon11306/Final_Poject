
# Financial Data Analysis Using Machine Learning

## Project Overview
This project aims to analyze stock data by leveraging technical indicators and machine learning models to predict trends. By combining feature engineering with neural network models, we assess and forecast potential price movements.

## Objectives
- Extract and calculate meaningful technical indicators from historical stock data.
- Build machine learning models to evaluate and predict stock price trends.
- Compare model performance to determine the most effective approach for stock trend prediction.

## Data Source
- **Dataset**: The analysis uses stock data stored in it one individual DataFrame, which includes:
  - **High Prices**: The highest stock prices in a given period.
  - **Low Prices**: The lowest stock prices in a given period.
  - **Close Prices**: The stock prices at the end of the trading period.

## Feature Engineering
Several technical indicators were calculated to capture different aspects of stock movement and volatility:
1. **Relative Strength Index (RSI)**: Indicates momentum and potential overbought/oversold conditions.
2. **Percentage Price Oscillator (PPO)**: Measures momentum by comparing moving averages.
3. **Rate of Change (ROC)**: Captures trend shifts based on percentage changes over a set period.
4. **Williams %R**: Highlights potential overbought and oversold levels.
5. **Stochastic Oscillator (%K and %D)**: Tracks price positioning relative to highs and lows.
6. **Average True Range (ATR)**: Reflects market volatility.

## Models
This project involves the development of two neural network models, each built with different frameworks:

### 1. Keras Sequential Neural Network
- **Model Structure**:
  - Input layer with nodes corresponding to feature count.
  - Two hidden layers with 12 and 6 nodes (Sigmoid activation).
  - Output layer with a single node (Sigmoid activation) for binary classification.
- **Training**: Trained over 25 epochs, with an evaluation of accuracy on the test set.
  
### 2. PyTorch Neural Network
- **Model Structure**:
  - Custom Dataset class for DataLoader batch processing.
  - Input layer, a hidden layer with 64 nodes (ReLU activation), and an output layer with 1 node (Sigmoid activation).
- **Training**: 50 epochs with Binary Cross-Entropy Loss and Adam Optimizer.

## Results
Both Keras and PyTorch models achieved comparable performance:
- **Keras Model Accuracy**: ~83%
- **PyTorch Model Accuracy**: ~82%
  
The models demonstrated successful trend prediction capabilities. Further optimization and tuning could improve results and generalizability.

## Future Work
Potential areas for further exploration include:
- Experimenting with more complex model architectures, such as CNNs or LSTMs.
- Fine-tuning model parameters and feature selection to improve accuracy.
- Exploring additional technical indicators or time series analysis methods.

## How to Run
1. Clone the repository and install required packages.
2. Run the notebook file to see the full code and training process.
3. View the model evaluation results to understand performance metrics.

## Questions
Please feel free to ask questions or suggest improvements! Contributions are welcome to expand and refine the project.
