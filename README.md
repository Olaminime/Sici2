# SMC ICT Trading Indicator for TradingView

## Overview
This Pine Script indicator combines Smart Money Concepts (SMC), Inner Circle Trader (ICT) principles, RSI divergence, and momentum indicators to identify optimal trade setups on 15-minute charts. The indicator automatically places Long and Short Position tools with precise entry, stop loss, and take profit levels.

## Features

### 🎯 **Core Trading Model**
- **Smart Money Concepts (SMC)**: Order block detection and market structure analysis
- **ICT Principles**: Fair Value Gaps (FVG) and liquidity level identification
- **RSI Divergence**: Momentum confirmation with customizable overbought/oversold levels
- **Trend Analysis**: Multi-timeframe EMA analysis (9, 21, 50)
- **Risk Management**: ATR-based stop loss with configurable risk-reward ratios

### 📊 **Visual Elements**
- **Long/Short Position Tools**: Automatically placed boxes with entry, SL, and TP levels
- **Order Blocks**: Visual representation of supply/demand zones
- **Fair Value Gaps**: Highlighted price gaps for potential reversal areas
- **Liquidity Levels**: Recent highs and lows for liquidity sweeps
- **Moving Averages**: EMA 9, 21, and 50 for trend confirmation
- **Signal Shapes**: Triangle markers for entry signals

### ⚙️ **Customizable Parameters**
- RSI Length and Levels (default: 14, 70/30)
- EMA Periods (default: 9, 21, 50)
- Risk-Reward Ratio (default: 2.0)
- ATR Multiplier for Stop Loss (default: 1.5)
- Order Block Detection Settings
- Visual Display Options

## How It Works

### Long Entry Conditions
1. **Trend**: EMA 9 > EMA 21 > EMA 50 (uptrend)
2. **Order Block**: Bullish order block detected (strong move up + consolidation)
3. **RSI**: RSI oversold with bullish divergence
4. **Fair Value Gap**: Bullish FVG present
5. **Price Action**: Close above order block low

### Short Entry Conditions
1. **Trend**: EMA 9 < EMA 21 < EMA 50 (downtrend)
2. **Order Block**: Bearish order block detected (strong move down + consolidation)
3. **RSI**: RSI overbought with bearish divergence
4. **Fair Value Gap**: Bearish FVG present
5. **Price Action**: Close below order block high

### Risk Management
- **Stop Loss**: ATR-based calculation (ATR × multiplier)
- **Take Profit**: Risk amount × risk-reward ratio
- **Minimum RR**: 1:2 ratio (configurable up to 1:10)

## Installation

1. Copy the Pine Script code from `smc_ict_trading_indicator.pine`
2. Open TradingView and go to Pine Editor
3. Paste the code and click "Add to Chart"
4. Customize parameters in the indicator settings
5. Apply to 15-minute chart for optimal results

## Usage Tips

### Best Practices
- Use on 15-minute charts for optimal signal quality
- Combine with higher timeframe trend analysis
- Wait for confluence of multiple signals
- Always respect stop loss levels
- Consider market session times (London/NY overlap preferred)

### Signal Interpretation
- **Green Triangle Up**: Long entry signal
- **Red Triangle Down**: Short entry signal
- **Green Boxes**: Bullish order blocks
- **Red Boxes**: Bearish order blocks
- **Lime Boxes**: Bullish fair value gaps
- **Fuchsia Boxes**: Bearish fair value gaps

### Risk Management
- Default 1:2 risk-reward ratio
- ATR-based stop loss for volatility adjustment
- Position sizing based on account risk tolerance
- Never risk more than 1-2% per trade

## Technical Specifications

- **Pine Script Version**: v4 (compatible with TradingView)
- **Chart Timeframe**: Optimized for 15-minute charts
- **Maximum Elements**: 500 boxes, 500 lines, 500 labels
- **Real-time Updates**: Yes, updates with each new bar
- **Alert Support**: Built-in alert conditions for signals

## Customization

### Input Parameters
```pinescript
// RSI Settings
rsi_length = 14
rsi_overbought = 70
rsi_oversold = 30

// Moving Averages
ema_fast = 9
ema_slow = 21
ema_trend = 50

// Risk Management
risk_reward_ratio = 2.0
atr_multiplier = 1.5
atr_length = 14

// Order Block Detection
ob_lookback = 5
ob_min_size = 3
```

### Visual Settings
- Toggle order blocks display
- Toggle fair value gaps display
- Toggle liquidity levels display
- Toggle signal markers display

## Alerts

The indicator includes built-in alert conditions:
- **Long Entry Signal**: Triggers when all long conditions are met
- **Short Entry Signal**: Triggers when all short conditions are met

## Disclaimer

This indicator is for educational and informational purposes only. Trading involves substantial risk of loss and is not suitable for all investors. Past performance is not indicative of future results. Always conduct your own research and consider your risk tolerance before trading.

## Support

For questions or issues with the indicator:
1. Check the Pine Script console for any errors
2. Verify all input parameters are within valid ranges
3. Ensure you're using Pine Script v4 compatible version
4. Test on a demo account before live trading

---

**Version**: 1.0  
**Last Updated**: 2024  
**Compatibility**: Pine Script v4, TradingView