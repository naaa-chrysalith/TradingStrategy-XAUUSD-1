# Indicators Reference Guide

**Focus**: MQL5 indicators for XAUUSD day trading  
**Timeframe**: 5-minute charts

## 📊 Active Indicators

### 1. Bollinger Bands

**What It Does**: Identifies overbought/oversold conditions and volatility.

**Settings (5-min)**:
- Period: 20
- Standard Deviation: 2
- Applied Price: Close

**How to Use**:
Long Signal:

Price touches lower band


Volume increase


= Potential bounce/reversal

Short Signal:

Price touches upper band


Volume increase


= Potential reversal


**Squeeze Detection**:
- When bands are close together = low volatility
- Next breakout will be strong = watch for direction

### 2. ATR (Average True Range)

**What It Does**: Measures market volatility.

**Settings (5-min)**:
- Period: 14
- Applied Price: High-Low

**How to Use**:
Current ATR > Average ATR (last 20 periods) = High volatility, good for trading
Current ATR < Average ATR = Low volatility, choppy, avoid or tight stops

**Stop Loss Sizing**:
Stop Loss = Current Price ± (ATR × 1.5)
Example:

XAUUSD at 2410.50
ATR (14) = 1.67
SL = 2410.50 - (1.67 × 1.5) = 2408.00 (risk = 2.50)


### 3. VWAP (Volume Weighted Average Price)

**What It Does**: Shows average price weighted by volume.

**Settings**:
- Period: Since market open (intraday)

**How to Use**:
Price > VWAP = Buyers in control (bullish)
Price < VWAP = Sellers in control (bearish)
Reversal at VWAP = Strong support/resistance

### 4. Volume Profile

**What It Does**: Shows volume distribution at different price levels.

**How to Use**:
High volume levels = Support/Resistance zones
Value Area = Where 70% of trading happens
Entry: At high volume support
Exit: At high volume resistance

### 5. Bollinger Squeeze Pattern

**What It Does**: Identifies low volatility before big moves.

**Pattern**:
When:

Bollinger Bands squeeze (very narrow)
Hold for 5-10 candles

Then:
Breakout in one direction = Strong follow-through
(Usually continues for 20-50+ pips)

**Trading Squeeze**:
Long After Squeeze:

Wait for bands to widen upward
Enter on first higher candle
SL = Recent low + ATR

Short After Squeeze:

Wait for bands to widen downward
Enter on first lower candle
SL = Recent high + ATR


## 📈 Indicator Setup in MT5

### Adding Indicators to Chart

1. Open MT5 → Charts tab
2. Right-click on chart → Indicators
3. Choose from list or search
4. Adjust settings as specified above
5. Click OK

### Indicator Color Customization

(Optional but helps visibility)

- Bollinger Bands: Use contrast color (e.g., blue/red)
- ATR: Separate window below
- VWAP: Use different color from price
- Volume: Below chart

## 🔄 Indicator Combination Rules

**Never rely on single indicator!**

### Good Combinations

**Setup 1: BB + ATR**
Entry when:
✅ Price bounces from BB
✅ ATR > 1.2 × average ATR
✅ Volume increases

**Setup 2: VWAP + BB**
Entry when:
✅ Price near VWAP
✅ At same level as BB
✅ Reversal pattern forms

**Setup 3: Squeeze + Volume**
Entry when:
✅ Bollinger Squeeze detected (narrow bands)
✅ Volume increasing
✅ Breakout in progress

## ⚠️ Common Mistakes

❌ Using indicator as single signal  
❌ Trading against trend shown by VWAP  
❌ Ignoring ATR (over/under estimating risk)  
❌ Trading squeeze without breakout confirmation  
❌ Not checking volume for confirmation  

✅ Always combine 2+ indicators  
✅ Always confirm with volume  
✅ Always respect ATR for stop loss  
✅ Always wait for breakout after squeeze  

## 📊 Indicator Values Tracking

Track actual indicator values as you trade:
Date: 2026-05-11
Time: 20:30
BB Upper: 2413.50
BB Lower: 2407.50
BB Middle: 2410.50
ATR(14): 1.67
VWAP: 2410.75
Volume: Above avg
Entry: 2408.00 (BB bounce)
Result: Hit TP1

## 🎓 Learning Resources

- [Bollinger Bands - Investopedia](https://www.investopedia.com/)
- [ATR Explained](https://en.wikipedia.org/wiki/Average_true_range)
- [VWAP Trading](https://www.tradingview.com/)

---

**Updated**: 2026-05-10  
**Review Frequency**: Monthly