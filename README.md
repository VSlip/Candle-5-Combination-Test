Overview

The project processes historical candlestick data to:

Categorize each candlestick as green (bullish), red (bearish), or neutral.

Combine candlestick patterns into sequences.

Identify sequences that consistently predict green or red candlesticks.

Output the most predictive combinations with their success rates.

Features

Categorization of candlesticks based on open, close, high, and low prices.

Detection of predictive candlestick sequences.

Calculation of success rates for each sequence.

Output of detailed statistics for both green and red predictions.

Installation

Clone the repository:

git clone https://github.com/your-username/candlestick-prediction.git

Navigate to the project directory:

cd candlestick-prediction

Install the required dependencies:

pip install pandas

Usage

Place your historical candlestick data file (CSV format) in the project directory. The CSV should contain the following columns:

OPEN

CLOSE

HIGH

LOW

Update the read_csv line in the code to match your data file name:

df = pd.read_csv("your_data_file.csv")

Run the script:

python candlestick_prediction.py

The results will be output as two DataFrames (df_green and df_red), showing the most predictive combinations for green and red candles, along with their statistics.

Data Description

The input data should be in CSV format and include the following columns:

OPEN: Opening price of the candlestick.

CLOSE: Closing price of the candlestick.

HIGH: Highest price of the candlestick.

LOW: Lowest price of the candlestick.

The script processes this data to calculate:

GREEN/RED: Categorization of each candlestick (1 for green, 0 for red).

combine1: Sequences of candlestick patterns.

Output

The script generates two DataFrames:

df_green: Predictive sequences for green candlesticks.

Columns: combinations, red, green, count, percentage

df_red: Predictive sequences for red candlesticks.

Columns: combinations, red, green, count, percentage

Example Output (Green Predictions):

combinations

red

green

count

percentage

[1, 1, 1, 1, 0]

140

151

291

51.89%

Example Output (Red Predictions):

combinations

red

green

count

percentage

[0, 0, 0, 0, 0]

725

163

888

81.64%

Contributing

Contributions are welcome! Please follow these steps:

Fork the repository.

Create a new branch for your feature or bug fix.

Submit a pull request with a clear explanation of your changes.

License

This project is licensed under the MIT License. See the LICENSE file for details.

