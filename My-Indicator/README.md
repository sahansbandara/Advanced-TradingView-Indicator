# SahanS Signal Indicator

A clean, confluence-based trading signal indicator for TradingView that combines multiple advanced analysis techniques into simple **BUY/SELL** signals.

---

## 📊 How It Works

The indicator uses a **confluence scoring system**. It runs 8 different analysis methods behind the scenes and counts how many give bullish or bearish signals. When the count reaches your selected threshold, a BUY or SELL signal appears.

```
Confluence Score ≥ Required Threshold → Signal Appears
```

---

## 🔍 Analysis Methods (Strategies Used)

### 1. RSI Divergence Detection
- **Bullish Divergence**: Price makes lower low, but RSI makes higher low → Reversal signal
- **Bearish Divergence**: Price makes higher high, but RSI makes lower high → Reversal signal
- Uses 14-period RSI with 5-bar pivot detection

### 2. Liquidity Sweep Detection
- **Bullish Sweep**: Price dips below swing low, then closes back above → Smart money grabbed liquidity
- **Bearish Sweep**: Price spikes above swing high, then closes back below → Smart money grabbed liquidity
- Uses 14-bar pivot points to identify swing levels

### 3. Smart Money Concepts (CHoCH)
- **Change of Character (CHoCH)**: Detects when trend direction changes
- Bullish CHoCH: Trend shifts from bearish to bullish
- Bearish CHoCH: Trend shifts from bullish to bearish
- Uses EMA 21, 50, 200 alignment for trend determination

### 4. Order Block Analysis
- **Bullish OB Touch**: Price enters a bullish order block zone → Buy opportunity
- **Bearish OB Touch**: Price enters a bearish order block zone → Sell opportunity
- Detects OB using volume pivots and price structure

### 5. Moving Average Crossovers
- **Bullish Cross**: EMA 21 crosses above EMA 50
- **Bearish Cross**: EMA 21 crosses below EMA 50

### 6. RSI Extreme Levels
- **Oversold** (RSI < 35): Adds to bullish score
- **Overbought** (RSI > 65): Adds to bearish score

### 7. MACD Momentum
- **Bullish Momentum**: MACD histogram increasing for 2+ bars
- **Bearish Momentum**: MACD histogram decreasing for 2+ bars

### 8. Trend Direction
- **Bullish Setup**: Price above EMA, trend is up, RSI not overbought
- **Bearish Setup**: Price below EMA, trend is down, RSI not oversold

---

## 🎯 Signal Strength Detection Method

Each analysis method adds **+1** to the confluence score when triggered:

| Condition | Bullish Score | Bearish Score |
|-----------|:-------------:|:-------------:|
| RSI Divergence | +1 | +1 |
| Liquidity Sweep | +1 | +1 |
| CHoCH (Structure Change) | +1 | +1 |
| Order Block Touch | +1 | +1 |
| MA Crossover | +1 | +1 |
| RSI Extreme | +1 | +1 |
| MACD Momentum | +1 | +1 |
| Trend Alignment | +1 | +1 |
| **Maximum Score** | **8** | **8** |

### Threshold Settings

| Setting | Required Score | Signal Frequency |
|---------|:--------------:|------------------|
| Conservative | 4+ | Fewer signals, higher quality |
| Medium | 3+ | Balanced approach |
| Aggressive | 2+ | More signals, faster entries |

### Example
```
Current Bar Analysis:
- RSI Divergence: YES (+1)
- Liquidity Sweep: YES (+1)  
- Order Block Touch: YES (+1)
- Others: NO

Bullish Score = 3

If Setting = "Medium" (requires 3) → BUY SIGNAL ✅
If Setting = "Conservative" (requires 4) → No Signal ❌
```

---

## ⚙️ Settings

| Setting | Options | Description |
|---------|---------|-------------|
| Signal Strength | Conservative / Medium / Aggressive | Confluence threshold |
| Show Trend Background | On/Off | Green (bull) / Red (bear) background |
| Show Info Panel | On/Off | Top-right score display |
| Buy/Sell Colors | Color picker | Customize signal colors |
| Signal Size | Tiny/Small/Normal/Large | Arrow size |
| Show MAs | On/Off | Display EMA lines |
| Show Divergence | On/Off | Show divergence dots |
| Show Liquidity | On/Off | Show sweep markers |

---

## 📈 Usage Guide

1. **Add to Chart**: Apply indicator in TradingView
2. **Choose Strength**: Select Conservative/Medium/Aggressive
3. **Watch for Signals**: 
   - 🟢 Green Triangle (BUY) - below candle
   - 🔴 Red Triangle (SELL) - above candle
4. **Check Info Panel**: See real-time confluence scores
5. **Set Alerts**: Enable alerts for notifications

---

## 🔔 Alerts

- `BUY Signal` - Triggered when buy conditions met
- `SELL Signal` - Triggered when sell conditions met

---

## 📝 Version History

- **v2.0** - Simplified edition with clean signals
- **v1.0** - Initial release with full visuals

---

*Created by SahanS*
