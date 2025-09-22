# Advanced VWAP Reclaim Strategy with ATR Filter & Bracket Orders

## Overview  
This Pine Script strategy implements an advanced intraday trading system based on VWAP reclaim signals combined with ATR-based stop loss and take profit levels. It features time window filtering and enforces a daily trade limit, making it a robust solution for intraday traders.

## Strategy Features  
- *VWAP Reclaim Entry:* Enters long positions when price crosses above the VWAP after being below it.  
- *ATR-Based Risk Management:* Dynamic stop loss and take profit levels calculated using Average True Range (ATR) multipliers.  
- *Intraday Time Window:* Trades are only taken within the user-defined market session (default 9:30 AM to 3:30 PM EST).  
- *Max Trades Per Day:* Limits the number of trades executed daily to control overtrading.  
- *Bracket Orders:* Entry, stop loss, and take profit orders are managed simultaneously for better risk control.  
- *Alert Conditions:* Supports alerts for entry signals to integrate with automation platforms like Zapier and Alpaca.

## Performance Summary (Backtested on AAPL)  
![Performance Overview](assests/overview2.png)
![Trade Analysis](assests/trade-analysis.png)

- Total Trades: 365  
- Win Rate: 36.16%  
- Average P&L: +$569.81 (0.57%)  
- Total Return: +20.8%
- Max Drawdown: 18.18%  

*Results based on historical data from Dec 1980 to Sep 2025.*

How to Use  
1. Copy the `advanced_vwap.pine` script into TradingView’s Pine Editor.  
2. Adjust session times, ATR settings, and trade limits via inputs to match your preferences.  
3. Add alerts for entry signals to connect with webhook services.  
4. For full automation, integrate with Zapier to receive alerts and use Alpaca API to place bracket orders automatically.

Future Enhancements  
- Implement short trade logic and improved exit strategies.  
- Add logging of trades to Google Sheets for detailed tracking.  
- Build a no-code dashboard for easier parameter adjustments.

---
