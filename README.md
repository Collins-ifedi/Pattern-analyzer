
Pattern Analyzer Module

This module detects common candlestick patterns and trend structures within historical cryptocurrency price data. It supports both traditional candlestick analysis and custom rule-based pattern recognition.

Purpose

The goal of this module is to help the AI trading assistant identify known bullish or bearish reversal/continuation patterns based on historical price action. These patterns are used as additional signals to inform trading decisions.

Key Features

Candlestick Pattern Detection: Utilizes TA-Lib to identify well-known candlestick formations such as Doji, Engulfing, Hammer, and Shooting Star.

Custom Rule-Based Analysis: Defines patterns based on conditions such as price breaking above or below support/resistance zones or forming local tops/bottoms.

Trend Structure Identification: Recognizes local highs and lows to infer potential breakout or breakdown points.

Pattern Labeling: Classifies detected formations as either "Bullish" or "Bearish" to simplify downstream interpretation.

Timestamped Results: Provides analysis with reference to the latest time index in the dataset.


Input Requirements

The module expects a pandas.DataFrame with standard OHLCV data:

open

high

low

close

volume


The DataFrame must be sorted in ascending chronological order for correct analysis.

Output

The module returns:

A list of dictionaries, where each dictionary represents a detected pattern.

Each result includes:

Pattern name (e.g., "Bullish Engulfing", "Doji", etc.)

Type (Bullish or Bearish)

Source (e.g., TA-Lib or Rule-Based)

Timestamp of occurrence



Integration

This module is designed to be used alongside:

Technical indicator modules (e.g., RSI, MACD, EMA)

LSTM or ML-based prediction models

Anomaly detection systems

Sentiment analysis for signal validation


It can be triggered on a periodic basis (e.g., hourly or per candle) as part of a real-time or batch trading pipeline.

Dependencies

Python 3.8+

pandas

ta-lib (for candlestick detection)


Ensure TA-Lib is correctly installed on your environment, including the shared library, as it's a native extension.

File Location

Module path: cryptsignal/pattern_analyzer.py


License

This file is open-source and released under the MIT License. Feel free to modify or extend it for personal or commercial use.

Author

Developed as part of a comprehensive AI-driven crypto trading assistant project by Chukwujiekwu Collins Ifedi.


---
