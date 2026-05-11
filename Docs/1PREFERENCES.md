# Trading Preferences & Configuration

**Trader**: naaa-chrysalith  
**Last Updated**: 2026-05-10

## 🎯 Primary Focus: Day Trading XAUUSD

### Account & Risk Management

| Parameter | Value |
|-----------|-------|
| **Account Risk Per Trade** | 20% |
| **Position Size Calculation** | (Account Size × 20%) / Stop Loss Points |
| **Daily Trade Limit** | Max 3 trades (TBD) |
| **Daily Loss Limit** | 3 × 20% = 60% max daily loss |

⚠️ **Note**: 20% per trade is aggressive. Consider reducing to 2-5% for sustainability.

### Market Focus

| Property | Value |
|----------|-------|
| **Instrument** | XAUUSD (Gold/US Dollar) |
| **Timeframe** | 5-minute |
| **Session** | London/US Session |
| **Analysis Time** | Afternoon/Evening WIB (13:00-22:00) |
| **Entry Time** | Evening WIB (18:00-23:00) |
| **Platform** | MetaTrader 5 (MQL5) |

### Market Hours (WIB = UTC+7)

| Market | WIB Time | UTC Time |
|--------|----------|----------|
| London Open | 15:00 (3 PM) | 08:00 |
| US Open | 21:30 (9:30 PM) | 14:30 |
| Peak Liquidity | 21:30-23:00 | 14:30-16:00 |

## 📊 Strategy Focus

### Active Development
1. **SimpleScalper** - 5-min scalping
2. **VolumeVolatility** - Bollinger Bands + ATR
3. **PriceAction** - Support/Resistance levels

### Indicators & Tools (Active Learning)

Based on recent study:
- ✅ **Bollinger Bands** - Entry/Exit signals
- ✅ **ATR (Average True Range)** - Volatility measurement & Stop Loss sizing
- ✅ **VWAP** - Volume-weighted average price
- ✅ **Volume Profile** - Support/Resistance identification
- ✅ **Bollinger Squeeze** - Low volatility before breakout

## 📋 Trading Rules

### Entry Conditions (All must be met)
- [ ] Bollinger Bands setup (squeeze or breakout)
- [ ] ATR indicates adequate volatility
- [ ] Price near identified support/resistance
- [ ] Volume confirmation
- [ ] During London/US session
- [ ] No major news events in next 1 hour

### Exit Conditions

| Exit Type | Rule |
|-----------|------|
| **Stop Loss** | ATR × 1.5 (to be optimized) |
| **Take Profit 1** | Risk × 1.5 |
| **Take Profit 2** | Risk × 2.5 |
| **Time-Based** | 4 hours from entry or 1 hour before session close |

### Risk Management (Must Follow)

- ✅ Always use stop loss
- ✅ Minimum Risk/Reward ratio: 1:1.5
- ✅ Never average down losing trades
- ✅ No revenge trading
- ✅ Max 3 trades per day
- ✅ Stop trading if daily loss limit reached

## 🔄 Secondary Focus: Swing Trading Forex (Future)

### Timeline
- **Start**: After mastering Day Trading (≈3-6 months)
- **Instruments**: EUR/USD, GBP/USD (to be decided)
- **Timeframes**: 4-hour, Daily
- **Platform**: TradingView (Pine Script)

### Learning Path
1. Study swing trading theory
2. Identify swing trading setups
3. Backtest strategies
4. Start with small live trades

## 📈 Performance Targets

### Short Term (Next 1 Month)
- [ ] Consistent profitable backtest results
- [ ] All strategies tested on XAUUSD
- [ ] Trading rules documented

### Medium Term (3 Months)
- [ ] Live trading with small position sizes
- [ ] Achieve consistent profitability
- [ ] Optimize parameters

### Long Term (6+ Months)
- [ ] Implement swing trading strategies
- [ ] Scale position sizes
- [ ] Diversify to other instruments

## 🛠️ Tools & Setup

- **Broker**: (TBD - Requires stable, low-spread forex broker)
- **Platform**: MetaTrader 5
- **Data Source**: Broker's historical data
- **Backtesting**: Strategy Tester in MT5
- **Analysis**: TradingView (charts) + MT5 (trading)

## 📝 File Locations

- **EA Code**: `MQL5 - Active Trading/XAUUSD-DayTrading/`
- **Historical Data**: `Data/XAUUSD/`
- **Backtest Results**: `Tests/`
- **Documentation**: `Docs/`
- **Development Notes**: `MQL5 - Active Trading/Development/notes.md`

---

**Status**: Active (Day Trading Focus)  
**Last Review**: 2026-05-10  
**Next Review**: 2026-06-10