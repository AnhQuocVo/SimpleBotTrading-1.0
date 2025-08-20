# Simple-Bot-Trading 1.0
My first time I learn to code a bot trade.

## Workflow
1. **Import Libraries and Configuration**
    -  The bot imports necessary libraries: `pandas`, `pandas_ta`, OANDA API modules, and a config file containing API credentials.

2. **Setup OANDA Connection**
   - Initializes the OANDA API client using the API key from the config file.

3. **Define Trading Parameters**
   - Sets the trading timeframe (e.g., `"M1"`) and instrument (e.g., `"GBP_JPY"`).

4. **Fetch Market Data**
   - Fetches candle data from OANDA using the `get_candles()` function and converts it to a pandas DataFrame.

5. **Calculate Technical Indicators**
   - Calculates EMAs (5 and 8 periods) and ATR (14 periods) using `pandas_ta` in the `calculate_indicators()` function.

6. **Signal Generation**
   - Checks for EMA crossover signals in the `ema_crossover()` function. If a buy signal is detected (EMA 5 crosses above EMA 8), it calculates stop loss and take profit levels.

7. **Order Placement**
   - Places a market order with calculated stop loss and take profit using the `place_order()` function.

8. **Main Bot Loop**
   - The `run_bot()` function runs an infinite loop, checking for new candles every minute, updating indicators, and executing trades when signals are detected.

9. **Run the Bot**
   - The bot starts by calling `run_bot()`.

