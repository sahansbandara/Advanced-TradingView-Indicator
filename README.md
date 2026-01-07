# SahanS Full Indicator

A comprehensive, all-in-one TradingView indicator that combines **Divergence Detection, Smart Money Concepts (SMC), Order Blocks, Liquidity Swings, and Moving Averages** into a single, powerful tool.

---

## ✨ Features

This indicator merges 5 major analysis systems:

| Feature | Description |
|---------|-------------|
| **Divergence Detector** | Identifies RSI, MACD, Stochastic, CCI, and other divergences |
| **Smart Money Concepts (SMC)** | Detects market structure breaks (BOS/CHoCH) |
| **Order Blocks (OB)** | Automatically draws bullish and bearish order block zones |
| **Liquidity Swings** | Highlights key swing highs and lows for liquidity |
| **4 Moving Averages** | Customizable EMA lines for trend analysis |

---

## 🔧 Configuration Options

### Divergence Settings
| Option | Description | Default |
|--------|-------------|---------|
| Pivot Period | Lookback period for divergence pivots | 5 |
| Source | Close or High/Low for pivot points | Close |
| Divergence Type | Regular, Hidden, or Both | Regular |
| Indicators | RSI, MACD, MACD Hist, Stoch, CCI, Momentum, OBV, VWmacd, CMF, MFI | All enabled |
| Show Divergence Number | Display count of divergences | On |

### SMC Settings
| Option | Description | Default |
|--------|-------------|---------|
| SMC Window | Bars to analyze for structure | 5000 |
| Show Swing Structure | Display BOS/CHoCH labels | On |
| Swing Limit | Maximum structure labels | 100 |
| Bullish/Bearish Color | Structure label colors | Green/Red |

### Order Block Settings
| Option | Description | Default |
|--------|-------------|---------|
| Show Order Blocks | Display OB zones | On |
| OB Show Last | Number of OBs to display | 5 |
| Bullish/Bearish OB Color | Zone fill colors | Green/Red (80% transparency) |
| OB Mitigation | Close or Wick mitigation | Close |

### Liquidity Swing Settings
| Option | Description | Default |
|--------|-------------|---------|
| Pivot Length | Swing detection lookback | 14 |
| High/Low Color | Liquidity level line colors | Red/Teal |

### Moving Averages Settings
| Option | Length | Default Color |
|--------|--------|---------------|
| MA 1 | 20 | Yellow |
| MA 2 | 50 | Blue |
| MA 3 | 100 | Red |
| MA 4 | 200 | White |

---

## 📈 How to Use

1.  **Add to TradingView**: Copy the script from `My-Indicator/SahanS-Indicator.pine` and paste it into TradingView's Pine Editor.
2.  **Add to Chart**: Click "Add to Chart".
3.  **Configure Settings**: Open the indicator settings to enable/disable features and customize colors.

### Understanding the Visuals
-   **`D` Circle Below Bar (Green)**: Bullish Divergence detected.
-   **`D` Circle Above Bar (Red)**: Bearish Divergence detected.
-   **`BOS` Label**: Break of Structure — a key level has been broken.
-   **Colored Boxes**: Order Blocks (Green = Bullish, Red = Bearish).
-   **Dashed Lines**: Liquidity levels (recent swing highs/lows).
-   **Solid Lines (EMA)**: 4 Moving Averages for trend context.
-   **Background Tint**: Green = Bullish Trend, Red = Bearish Trend.

---

## 🔔 Alerts

You can set alerts based on the plotshapes for divergence signals.

---

## 📝 Version History

-   **v3.0** - Full combined indicator (Divergence + SMC + OB + Liquidity + MAs)
-   **v2.0** - Simplified signal indicator
-   **v1.0** - Initial release

---

*Created by SahanS*
