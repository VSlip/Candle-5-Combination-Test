# Candlestick Pattern Prediction

This project explores candlestick patterns in stock market data to identify specific combinations that could predict the movement of the next candle. Using historical stock data, the script analyzes patterns and outputs combinations with high predictive accuracy.

## Project Overview

Candlestick charts are widely used in technical analysis. This project aims to:
- Identify unique combinations of candlestick patterns.
- Determine the predictive value of each combination.
- Categorize combinations into bullish or bearish indicators based on historical data.

## Features

- **Candlestick Analysis**: Differentiates between green (bullish) and red (bearish) candles based on open and close prices.
- **Combination Detection**: Evaluates sequences of candlesticks and identifies patterns.
- **Validation**: Calculates the accuracy and frequency of combinations that predict the next candle's direction.
- **Result Segmentation**: Outputs valid combinations into `df_green` (bullish predictions) and `df_red` (bearish predictions) dataframes.

## Data Requirements

The project uses a CSV file containing historical stock data with the following columns:
- `OPEN`: Opening price of the stock.
- `CLOSE`: Closing price of the stock.
- `HIGH`: Highest price during the time period.
- `LOW`: Lowest price during the time period.

## Installation and Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/VSlip/Candle-5-Combination-Test.git
   ```

2. Navigate to the project directory:
   ```bash
   cd Candle-5-Combination-Test
   ```

3. Install the required dependencies:
   ```bash
   pip install pandas
   ```

4. Add your dataset file (e.g., `AAPLD.csv`) to the project directory.

## Usage


The script outputs two DataFrames:
- `df_green`: Contains combinations predicting a bullish outcome.
- `df_red`: Contains combinations predicting a bearish outcome.

Both DataFrames include the following fields:
- `combinations`: The candlestick sequence.
- `red`: Count of bearish predictions.
- `green`: Count of bullish predictions.
- `count`: Total occurrences of the combination.
- `percentage`: Accuracy of the prediction in percentage.

## Example Output

### Green Predictions (`df_green`):
| Index | Combinations       | Red | Green | Count | Percentage |
|-------|--------------------|-----|-------|-------|------------|
| 0     | [1, 1, 1, 1, 0]   | 140 | 151   | 291   | 51.89%     |
| 1     | [0, 1, 1, 0, 1]   | 127 | 149   | 276   | 53.98%     |

### Red Predictions (`df_red`):
| Index | Combinations       | Red | Green | Count | Percentage |
|-------|--------------------|-----|-------|-------|------------|
| 0     | [0, 0, 0, 0, 0]   | 725 | 163   | 888   | 81.64%     |
| 1     | [0, 0, 0, 0, 1]   | 181 | 133   | 314   | 57.64%     |

## Customization

- Update the `AAPLD.csv` file to analyze data for different stocks.
- Modify the pattern detection logic to include additional candlestick attributes such as Doji or engulfing patterns.

## Limitations

- The results depend heavily on the quality and timeframe of the input data.
- No guarantee of future prediction accuracy due to the volatile nature of stock markets.


## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

### Author
Developed by [VSlip](https://github.com/VSlip).
