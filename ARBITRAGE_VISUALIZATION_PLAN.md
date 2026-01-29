# Currency & Precious Metals Arbitrage Visualization Tool

## Executive Summary

This document outlines a comprehensive tool for identifying and visualizing arbitrage opportunities across currencies and precious metals. The tool will provide traders with real-time insights into pricing discrepancies, cross-rate inefficiencies, and triangular arbitrage opportunities.

---

## 1. Asset Universe

### 1.1 Major Currencies
| Currency | Code | Characteristics |
|----------|------|-----------------|
| US Dollar | USD | Global reserve currency, base for most pairs |
| Euro | EUR | Second most traded, eurozone benchmark |
| British Pound | GBP | High volatility, Brexit sensitivity |
| Japanese Yen | JPY | Safe haven, carry trade funding |
| Swiss Franc | CHF | Safe haven, gold correlation |
| Australian Dollar | AUD | Commodity currency, China proxy |
| Canadian Dollar | CAD | Oil correlation, commodity currency |
| New Zealand Dollar | NZD | Commodity currency, dairy exports |
| Chinese Yuan | CNY/CNH | Managed float, growing importance |

### 1.2 Precious Metals
| Metal | Code | Characteristics |
|-------|------|-----------------|
| Gold | XAU | Safe haven, inflation hedge, central bank reserves |
| Silver | XAG | Industrial + precious, higher volatility |
| Copper | XCU | Industrial bellwether, economic indicator |
| Platinum | XPT | Industrial precious, automotive catalyst |
| Palladium | XPD | Automotive catalyst, supply constraints |

---

## 2. Most Interesting Combinations

### 2.1 Tier 1: Highest Priority Pairs (Core Arbitrage Opportunities)

#### Triangular Currency Combinations
These form the basis for classic triangular arbitrage detection:

```
Triangle 1: USD → EUR → GBP → USD
Triangle 2: USD → EUR → JPY → USD
Triangle 3: USD → GBP → JPY → USD
Triangle 4: USD → EUR → CHF → USD
Triangle 5: USD → AUD → JPY → USD
Triangle 6: EUR → GBP → CHF → EUR
```

#### Gold Cross-Currency Arbitrage
Gold priced in different currencies should maintain parity via FX rates:

```
XAU/USD vs XAU/EUR × EUR/USD
XAU/USD vs XAU/GBP × GBP/USD
XAU/USD vs XAU/JPY × JPY/USD
XAU/USD vs XAU/CHF × CHF/USD
```

### 2.2 Tier 2: Ratio Analysis Pairs

| Ratio | Historical Range | Significance |
|-------|------------------|--------------|
| Gold/Silver (XAU/XAG) | 40:1 to 100:1 | Mean reversion opportunity, historical avg ~65:1 |
| Gold/Copper | Variable | Economic sentiment indicator |
| Gold/Platinum | 0.8:1 to 2:1 | Platinum historically premium, now inverted |
| Silver/Copper | Variable | Industrial metals comparison |
| Gold/Oil | 10:1 to 40:1 | Inflation/deflation indicator |

### 2.3 Tier 3: Commodity Currency Correlations

```
AUD/USD ↔ Copper prices (Australia = major exporter)
CAD/USD ↔ Oil prices (Canada = major exporter)
AUD/USD ↔ Gold prices (Australia = major producer)
ZAR/USD ↔ Gold/Platinum (South Africa = major producer)
CLP/USD ↔ Copper (Chile = largest producer)
```

---

## 3. Core Visualizations

### 3.1 Real-Time Arbitrage Detection Matrix

**Purpose**: Instantly identify pricing discrepancies across all pairs

```
          USD    EUR    GBP    JPY    XAU    XAG
    USD    -    1.08   1.27   149.5  2015   23.45
    EUR   0.93    -    1.17   138.4  1866   21.71
    GBP   0.79  0.85    -     118.1  1587   18.47
    JPY   0.007 0.007 0.008    -     13.5   0.157
    XAU   ...
    XAG   ...
```

**Features**:
- Color coding: Green (opportunity), Yellow (watch), Red (efficient)
- Click any cell to see arbitrage path
- Real-time updates with websocket feeds

### 3.2 Triangular Arbitrage Network Graph

**Purpose**: Visualize all possible triangular arbitrage paths

```
              [USD]
             /  |  \
            /   |   \
         [EUR]--+--[GBP]
            \   |   /
             \  |  /
              [JPY]
                |
              [XAU]
```

**Features**:
- Nodes = Assets (currencies + metals)
- Edges = Exchange rates
- Edge thickness = Trading volume
- Edge color = Arbitrage opportunity strength
- Animated flow showing profitable paths

### 3.3 Cross-Rate Discrepancy Dashboard

**Purpose**: Compare implied vs quoted cross rates

| Cross Rate | Implied | Quoted | Discrepancy | Opportunity |
|------------|---------|--------|-------------|-------------|
| EUR/GBP | 0.8521 | 0.8519 | +0.02% | ⚪ None |
| EUR/JPY | 162.34 | 162.28 | +0.04% | 🟡 Watch |
| GBP/JPY | 190.42 | 190.55 | -0.07% | 🟢 Active |

### 3.4 Historical Ratio Charts

**Gold/Silver Ratio Chart**
```
Ratio
100 |                    *
 90 |              *    * *
 80 |        *    * *  *   *
 70 |   *   * *  *        *  *
 60 | ** * *                   *
 50 |*
    +---------------------------→ Time
    Historical mean: 65:1
    Current: 86:1 (Silver undervalued?)
```

**Features**:
- Bollinger bands for mean reversion signals
- Historical percentile indicator
- Alerts when ratio hits extremes

### 3.5 Correlation Heatmap

**Purpose**: Understand asset relationships for pair trading

```
        USD  EUR  GBP  JPY  CHF  AUD  XAU  XAG  XCU
   USD   1  -.89 -.85  .42  -.72 -.65 -.45 -.38 -.52
   EUR       1   .92 -.38   .85  .71  .52  .44  .58
   GBP           1   -.35   .78  .68  .48  .41  .55
   JPY                1    -.45 -.58  .35  .28 -.42
   CHF                      1    .62  .68  .55  .48
   AUD                            1   .45  .52  .78
   XAU                                 1   .88  .42
   XAG                                      1   .65
   XCU                                           1
```

**Color Scale**: -1 (Red) → 0 (White) → +1 (Green)

### 3.6 Spread Time Series

**Purpose**: Track historical spreads between related assets

```
Gold USD vs Gold EUR (converted)
Spread (bps)
  +50 |      *
  +25 |  *  * *    *
    0 |--*-------*---*--*-----  Mean
  -25 |            *   * *
  -50 |                   *
      +----------------------→ Time
```

### 3.7 Multi-Asset Comparison View

**Purpose**: Compare any N assets on normalized scale

```
                 Normalized Performance (Base 100)
   115 |                              XAU ___
   110 |                         ___---
   105 |              EUR ___---
   100 |===USD=========---============ Baseline
    95 |         ___---
    90 |    ___--- XAG
    85 |---
       +--------------------------------→ Time
```

### 3.8 Volatility Surface

**Purpose**: Compare volatility regimes across assets

| Asset | 1D Vol | 1W Vol | 1M Vol | 3M Vol | Vol Regime |
|-------|--------|--------|--------|--------|------------|
| EUR/USD | 0.4% | 1.2% | 2.8% | 5.1% | Low |
| GBP/USD | 0.6% | 1.8% | 4.2% | 7.8% | Elevated |
| XAU/USD | 0.8% | 2.1% | 4.8% | 9.2% | Normal |
| XAG/USD | 1.5% | 4.2% | 9.5% | 18.1% | High |

---

## 4. Advanced Analytics Features

### 4.1 Triangular Arbitrage Scanner

**Algorithm**:
```
For each triangle (A, B, C):
    rate_direct = A→C
    rate_implied = (A→B) × (B→C)
    discrepancy = |rate_direct - rate_implied| / rate_direct

    if discrepancy > threshold + transaction_costs:
        signal ARBITRAGE_OPPORTUNITY
```

**Output Table**:
| Triangle | Direct | Implied | Spread | Net Profit* | Action |
|----------|--------|---------|--------|-------------|--------|
| USD→EUR→GBP | 1.2705 | 1.2712 | 5.5 bps | 2.5 bps | BUY |
| USD→EUR→JPY | 149.52 | 149.48 | 2.7 bps | -0.3 bps | HOLD |

*After estimated transaction costs

### 4.2 Precious Metals Parity Monitor

**Concept**: Gold (and silver) should trade at equivalent prices globally when converted via FX

```
XAU/USD = 2015.50
XAU/EUR = 1866.20
EUR/USD = 1.0800

Implied XAU/USD via EUR = 1866.20 × 1.0800 = 2015.50 ✓ Parity
Actual spread: 0.00%
```

**Dashboard**: Show all metal/currency combinations with parity deviations

### 4.3 Mean Reversion Signals

For ratio pairs (Gold/Silver, etc.):
- Z-score from historical mean
- Bollinger band position
- RSI of ratio
- Time since last mean touch

```
Gold/Silver Ratio: 86.5
Historical Mean (10Y): 68.2
Z-Score: +2.1σ (Silver historically cheap)
Bollinger Position: Upper band (overbought)
Signal: STRONG SELL RATIO (Buy silver, sell gold)
```

### 4.4 Cross-Market Basis Tracker

Track the same asset across different markets:
- COMEX Gold vs LBMA Gold
- CME FX vs Interbank rates
- Spot vs Futures basis

---

## 5. Data Requirements

### 5.1 Real-Time Data Feeds

| Data Type | Source Options | Update Frequency |
|-----------|---------------|------------------|
| FX Spot Rates | Reuters, Bloomberg, OANDA | Tick/100ms |
| Precious Metals Spot | LBMA, COMEX, Kitco | 1s |
| Futures Prices | CME, COMEX | Tick |
| Order Book Depth | Exchange APIs | 100ms |

### 5.2 Historical Data

| Data Type | Granularity | History Depth |
|-----------|-------------|---------------|
| OHLCV | 1min, 5min, 1H, 1D | 10+ years |
| Tick Data | Individual ticks | 1-2 years |
| Fundamental | Daily | 20+ years |

### 5.3 Derived Data

- Implied cross rates
- Rolling correlations (various windows)
- Historical volatility
- Ratio time series
- Spread time series

---

## 6. Technical Architecture

### 6.1 System Components

```
┌─────────────────────────────────────────────────────────┐
│                    DATA LAYER                           │
├─────────────┬─────────────┬─────────────┬──────────────┤
│  FX Feeds   │ Metal Feeds │  Futures    │  Historical  │
│  (WebSocket)│ (WebSocket) │  (WebSocket)│  (REST API)  │
└──────┬──────┴──────┬──────┴──────┬──────┴───────┬──────┘
       │             │             │              │
       └─────────────┴──────┬──────┴──────────────┘
                            ▼
┌─────────────────────────────────────────────────────────┐
│                 PROCESSING LAYER                        │
├─────────────┬─────────────┬─────────────┬──────────────┤
│  Rate       │  Arbitrage  │  Analytics  │  Alert       │
│  Normalizer │  Scanner    │  Engine     │  Generator   │
└──────┬──────┴──────┬──────┴──────┬──────┴───────┬──────┘
       │             │             │              │
       └─────────────┴──────┬──────┴──────────────┘
                            ▼
┌─────────────────────────────────────────────────────────┐
│                 VISUALIZATION LAYER                     │
├─────────────┬─────────────┬─────────────┬──────────────┤
│  Matrix     │  Network    │  Charts     │  Dashboard   │
│  View       │  Graph      │  Library    │  Builder     │
└─────────────┴─────────────┴─────────────┴──────────────┘
```

### 6.2 Technology Stack (Recommended)

**Backend**:
- Python (data processing, analytics)
- FastAPI (REST endpoints)
- Redis (real-time data cache)
- PostgreSQL/TimescaleDB (historical storage)

**Frontend**:
- React/TypeScript
- D3.js (custom visualizations)
- Apache ECharts (standard charts)
- WebSocket client (real-time updates)

**Infrastructure**:
- Docker containers
- Kubernetes for scaling
- Grafana for monitoring

---

## 7. Key Metrics & Alerts

### 7.1 Arbitrage Opportunity Metrics

| Metric | Description | Alert Threshold |
|--------|-------------|-----------------|
| Triangle Spread | Discrepancy in triangular arbitrage | > 5 bps |
| Cross-Rate Deviation | Implied vs quoted difference | > 3 bps |
| Metal Parity Spread | XAU in different currencies | > 10 bps |
| Ratio Z-Score | Distance from historical mean | > 2σ |

### 7.2 Market Condition Indicators

| Indicator | Description | Use Case |
|-----------|-------------|----------|
| Correlation Breakdown | When correlated assets diverge | Pair trade entry |
| Volatility Spike | Sudden vol increase | Risk management |
| Liquidity Drought | Bid-ask spread widening | Execution timing |
| Basis Blowout | Spot-futures divergence | Cash & carry arb |

---

## 8. User Interface Mockup

### 8.1 Main Dashboard Layout

```
┌────────────────────────────────────────────────────────────────┐
│  ARBITRAGE MONITOR           [Live] 🟢    Last: 14:32:05 UTC   │
├────────────────────────────────────────────────────────────────┤
│ ┌──────────────────────┐  ┌──────────────────────────────────┐ │
│ │   OPPORTUNITY FEED   │  │      TRIANGULAR ARBITRAGE        │ │
│ │                      │  │         NETWORK GRAPH            │ │
│ │ 🟢 USD→EUR→GBP +2.1bp│  │                                  │ │
│ │ 🟡 XAU EUR/USD +0.8bp│  │        [USD]──────[EUR]          │ │
│ │ 🟢 Au/Ag Ratio 86.5  │  │         / \        / \           │ │
│ │ ⚪ USD→JPY→EUR -0.2bp│  │      [GBP]─[JPY]─[CHF]           │ │
│ │                      │  │              \   /               │ │
│ └──────────────────────┘  │             [XAU]                │ │
│                           └──────────────────────────────────┘ │
├────────────────────────────────────────────────────────────────┤
│ ┌──────────────────────────────────────────────────────────┐   │
│ │                    CROSS-RATE MATRIX                      │   │
│ │       USD     EUR     GBP     JPY     XAU     XAG        │   │
│ │ USD    -    1.0800  1.2705  149.52  2015.5  23.45       │   │
│ │ EUR  0.9259   -     1.1764  138.44  1866.2  21.71       │   │
│ │ GBP  0.7871 0.8500    -     117.68  1586.5  18.47       │   │
│ │ ...                                                       │   │
│ └──────────────────────────────────────────────────────────┘   │
├────────────────────────────────────────────────────────────────┤
│ ┌────────────────────────────┐ ┌────────────────────────────┐  │
│ │    GOLD/SILVER RATIO       │ │    CORRELATION HEATMAP     │  │
│ │         86.5 (+2.1σ)       │ │                            │  │
│ │    ┌─────────────────┐     │ │   [Heatmap visualization]  │  │
│ │    │     ████        │     │ │                            │  │
│ │    │   ██    ██      │     │ │                            │  │
│ │    │ ██        ██    │     │ │                            │  │
│ │    └─────────────────┘     │ │                            │  │
│ └────────────────────────────┘ └────────────────────────────┘  │
└────────────────────────────────────────────────────────────────┘
```

---

## 9. Implementation Phases

### Phase 1: Foundation (Weeks 1-4)
- [ ] Set up data ingestion pipeline
- [ ] Implement core rate normalization
- [ ] Build basic cross-rate matrix
- [ ] Create historical data storage

### Phase 2: Core Analytics (Weeks 5-8)
- [ ] Implement triangular arbitrage scanner
- [ ] Build precious metals parity monitor
- [ ] Create ratio analysis engine
- [ ] Develop correlation calculator

### Phase 3: Visualization (Weeks 9-12)
- [ ] Build interactive cross-rate matrix
- [ ] Create network graph visualization
- [ ] Implement ratio charts with signals
- [ ] Build correlation heatmap

### Phase 4: Advanced Features (Weeks 13-16)
- [ ] Real-time alert system
- [ ] Backtesting framework
- [ ] Custom dashboard builder
- [ ] API for external integrations

### Phase 5: Polish & Scale (Weeks 17-20)
- [ ] Performance optimization
- [ ] Mobile-responsive design
- [ ] User authentication & preferences
- [ ] Documentation & training

---

## 10. Success Metrics

| Metric | Target | Measurement |
|--------|--------|-------------|
| Arbitrage Detection Latency | < 100ms | Time from price update to signal |
| False Positive Rate | < 5% | Signals that weren't executable |
| Data Freshness | < 500ms | Lag from source to display |
| Uptime | 99.9% | System availability |
| User Adoption | 80%+ daily active | Regular usage |

---

## 11. Risk Considerations

### 11.1 Execution Risks
- Arbitrage opportunities may close before execution
- Transaction costs may exceed theoretical profit
- Slippage in fast-moving markets

### 11.2 Data Risks
- Feed delays or outages
- Stale quotes appearing as opportunities
- Cross-exchange timing differences

### 11.3 Mitigation Strategies
- Include realistic transaction cost estimates
- Show opportunity age/freshness
- Require minimum profit threshold above costs
- Implement data quality monitoring

---

## 12. Appendix: Arbitrage Formulas

### Triangular Arbitrage
```
Given currencies A, B, C:
Profit = (1/Rate_AB) × Rate_BC × Rate_CA - 1

Example: USD → EUR → GBP → USD
If EUR/USD = 1.08, GBP/EUR = 0.85, USD/GBP = 1.27
Profit = (1/1.08) × 0.85 × 1.27 - 1 = 0.00% (no arbitrage)
```

### Cross-Rate Parity
```
Implied Cross Rate = Rate_A/Base × Rate_Base/B
Discrepancy = |Quoted - Implied| / Quoted

Example: EUR/GBP
Implied = EUR/USD × USD/GBP = 1.08 × 0.787 = 0.850
If Quoted = 0.852, Discrepancy = 0.23%
```

### Precious Metals Parity
```
XAU/USD should equal XAU/EUR × EUR/USD
Spread = XAU/USD - (XAU/EUR × EUR/USD)
```

---

*Document Version: 1.0*
*Last Updated: January 2026*
*Author: Arbitrage Analysis Team*
