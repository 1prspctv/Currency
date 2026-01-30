# Currency & Precious Metals Arbitrage Visualization Tool

## Executive Summary

This document outlines a comprehensive tool for identifying and visualizing arbitrage opportunities across currencies and precious metals. The tool will provide traders with real-time insights into pricing discrepancies, cross-rate inefficiencies, and triangular arbitrage opportunities.

---

## 1. Asset Universe

### 1.1 Major Currencies (G10)
| Currency | Code | Characteristics | Arbitrage Interest |
|----------|------|-----------------|-------------------|
| US Dollar | USD | Global reserve currency, base for most pairs | Base currency for all triangles |
| Euro | EUR | Second most traded, eurozone benchmark | High liquidity, tight spreads |
| British Pound | GBP | High volatility, Brexit sensitivity | Volatile = more opportunities |
| Japanese Yen | JPY | Safe haven, carry trade funding | Carry trade dislocations |
| Swiss Franc | CHF | Safe haven, gold correlation | SNB intervention creates gaps |
| Australian Dollar | AUD | Commodity currency, China proxy | Copper/gold correlation plays |
| Canadian Dollar | CAD | Oil correlation, commodity currency | Oil spread arbitrage |
| New Zealand Dollar | NZD | Commodity currency, dairy exports | AUD/NZD ratio mean reversion |
| Swedish Krona | SEK | Risk-on currency, EU trade exposure | EUR/SEK peg history |
| Norwegian Krone | NOK | Oil correlation, Scandinavian | Brent oil proxy trades |

### 1.2 Emerging Market Currencies (High Arbitrage Potential)

These markets have higher volatility, wider spreads, and less efficient pricing—creating more frequent arbitrage opportunities.

| Currency | Code | Characteristics | Why High Arb Potential |
|----------|------|-----------------|----------------------|
| Chinese Yuan | CNY/CNH | Managed float, dual market | **CNY/CNH spread = direct arb** |
| Hong Kong Dollar | HKD | USD peg (7.75-7.85 band) | **Peg stress = massive opportunity** |
| Singapore Dollar | SGD | Managed against basket | Basket composition plays |
| South Korean Won | KRW | Tech/semiconductor proxy | KOSPI correlation trades |
| Indian Rupee | INR | RBI managed, capital controls | Offshore/onshore spread (NDF) |
| Taiwan Dollar | TWD | Tech exports, China tensions | Semiconductor cycle proxy |
| Thai Baht | THB | Tourism/trade sensitive | Regional contagion plays |
| Malaysian Ringgit | MYR | Oil/palm oil correlation | Commodity spread trades |
| Indonesian Rupiah | IDR | Commodity exporter, high yield | Carry trade opportunities |
| Philippine Peso | PHP | Remittance flows, BPO sector | USD demand cycles |
| Mexican Peso | MXN | High carry, US trade exposure | **USMCA/nearshoring plays** |
| Brazilian Real | BRL | Commodity super-currency | **Iron ore/soy/coffee proxy** |
| Chilean Peso | CLP | **Copper pure play** | Direct copper correlation |
| Colombian Peso | COP | Oil exporter | Brent correlation |
| Peruvian Sol | PEN | Copper/gold mining | Metals proxy |
| Argentine Peso | ARS | Multiple exchange rates | **Blue dollar spread = huge arb** |
| South African Rand | ZAR | Gold/platinum correlation | **PGM mining proxy** |
| Turkish Lira | TRY | High volatility, policy risk | Extreme carry opportunities |
| Russian Ruble | RUB | Oil/gas, sanctions impact | Energy correlation (when tradeable) |
| Polish Zloty | PLN | EU convergence play | EUR/PLN mean reversion |
| Czech Koruna | CZK | CNB intervention history | Floor/ceiling plays |
| Hungarian Forint | HUF | High yield, EU tensions | Carry vs risk balance |
| Romanian Leu | RON | EU accession trajectory | Convergence trades |
| Israeli Shekel | ILS | Tech sector, safe haven | Regional risk premium |
| UAE Dirham | AED | USD peg | Oil cycle vs peg stress |
| Saudi Riyal | SAR | USD peg | **Oil stress = peg questions** |
| Kuwaiti Dinar | KWD | Basket peg, highest value | Stable reference rate |
| Egyptian Pound | EGP | Managed float, devaluations | **Post-deval opportunities** |
| Nigerian Naira | NGN | Multiple rates, oil dependent | Official/parallel spread |
| Kenyan Shilling | KES | East African hub | Regional trade flows |
| Ghanaian Cedi | GHS | Cocoa exporter | Cocoa correlation |
| Vietnamese Dong | VND | Manufacturing hub | Supply chain proxy |

### 1.3 Pegged & Managed Currencies (Special Arbitrage Cases)

These currencies create unique arbitrage opportunities when pegs come under stress.

| Currency | Peg/Band | Stress Indicators | Opportunity Type |
|----------|----------|-------------------|------------------|
| HKD | 7.75-7.85 to USD | HIBOR-LIBOR spread, forwards | Band boundary trades |
| DKK | 7.46 ± 2.25% to EUR | DNB reserves, intervention | Peg defense trades |
| BGN | 1.95583 to EUR | Currency board | EMU entry speculation |
| BAM | 1.95583 to EUR | Currency board (BiH) | Political risk premium |
| SAR | 3.75 to USD | Oil price, fiscal balance | Peg sustainability |
| AED | 3.6725 to USD | Oil price, diversification | Regional hub premium |
| CNY | Managed vs basket | PBOC fixing, reserves | Onshore/offshore gap |

### 1.4 Precious Metals
| Metal | Code | Characteristics | Key Arbitrage Plays |
|-------|------|-----------------|-------------------|
| Gold | XAU | Safe haven, inflation hedge, central bank reserves | Cross-currency parity, COMEX/LBMA basis |
| Silver | XAG | Industrial + precious, higher volatility | **Gold/Silver ratio (mean reversion)** |
| Platinum | XPT | Industrial precious, automotive catalyst | **Gold/Platinum inversion** |
| Palladium | XPD | Automotive catalyst, supply constraints | Platinum/Palladium substitution |
| Rhodium | XRH | Rarest precious metal, auto catalyst | Extreme volatility plays |

### 1.5 Industrial Metals
| Metal | Code | Exchange | Key Arbitrage Plays |
|-------|------|----------|-------------------|
| Copper | HG/XCU | COMEX/LME | **AUD correlation, COMEX/LME spread** |
| Aluminum | ALI | LME | China export arbitrage, energy costs |
| Zinc | ZNC | LME | Galvanizing demand, lead ratio |
| Nickel | NI | LME | **EV battery demand, Indonesia supply** |
| Lead | PB | LME | Battery demand, zinc/lead ratio |
| Tin | SN | LME | Semiconductor solder demand |
| Iron Ore | TIO | SGX/DCE | **BRL correlation, China steel demand** |

### 1.6 Energy Commodities
| Commodity | Code | Exchange | Key Arbitrage Plays |
|-----------|------|----------|-------------------|
| WTI Crude | CL | NYMEX | **WTI/Brent spread (key arb!)** |
| Brent Crude | BZ | ICE | CAD/NOK correlation |
| Natural Gas (US) | NG | NYMEX | **Henry Hub/TTF spread** |
| Natural Gas (EU) | TTF | ICE | JKM/TTF LNG arbitrage |
| Natural Gas (Asia) | JKM | CME | Seasonal Asia premium |
| Gasoline (RBOB) | RB | NYMEX | Crack spread vs crude |
| Heating Oil | HO | NYMEX | Seasonal patterns, crack spread |
| Uranium | UX | Spot/Term | **Nuclear renaissance plays** |
| Coal (Newcastle) | NCF | ICE | Asian demand, shipping costs |
| Carbon Credits | EUA | ICE | **Regulatory arbitrage, EU/UK spread** |

### 1.7 Agricultural Commodities
| Commodity | Code | Exchange | Key Arbitrage Plays |
|-----------|------|----------|-------------------|
| Wheat | ZW | CBOT | **CBOT/MATIF spread, Black Sea risk** |
| Corn | ZC | CBOT | Ethanol correlation, feed demand |
| Soybeans | ZS | CBOT | **BRL correlation, China demand** |
| Soybean Oil | ZL | CBOT | Biodiesel demand, palm oil ratio |
| Soybean Meal | ZM | CBOT | Crush spread |
| Coffee (Arabica) | KC | ICE | **BRL correlation, frost risk** |
| Coffee (Robusta) | RC | ICE | Arabica/Robusta spread |
| Cocoa | CC | ICE | **GHS/COP correlation, weather** |
| Sugar #11 | SB | ICE | BRL correlation, ethanol parity |
| Cotton | CT | ICE | India/US production shifts |
| Palm Oil | FCPO | BMD | **MYR correlation, biodiesel** |
| Rice | ZR | CBOT | Asian food security |
| Oats | ZO | CBOT | Weather sensitivity |
| Live Cattle | LE | CME | Feed cost spreads |
| Lean Hogs | HE | CME | China import demand |
| Orange Juice | OJ | ICE | Florida weather plays |

### 1.8 Strategic & Battery Metals (Emerging Opportunities)
| Metal | Trading Venue | Key Arbitrage Plays |
|-------|--------------|-------------------|
| Lithium | China futures, Chile spot | **EV demand, brine vs spodumene** |
| Cobalt | LME, physical | DRC supply concentration risk |
| Rare Earth Elements | China spot | **Export restrictions, Western reshoring** |
| Manganese | Physical | Battery chemistry shifts |
| Graphite | Physical | Anode material demand |
| Vanadium | Physical | Grid storage batteries |
| Molybdenum | Physical | Steel alloy demand |
| Tungsten | Physical | Industrial/defense demand |

### 1.9 Cryptocurrency (Optional Module)
| Asset | Code | Key Arbitrage Plays |
|-------|------|-------------------|
| Bitcoin | BTC | **Exchange spreads, futures basis, Kimchi premium** |
| Ethereum | ETH | ETH/BTC ratio, DeFi correlation |
| Tether | USDT | **1:1 peg deviation = warning sign** |
| USDC | USDC | USDT/USDC spread |
| Stablecoins | Various | Cross-stablecoin arbitrage |

---

## 2. Most Interesting Combinations

### 2.1 Tier 1: Highest Priority Pairs (Core Arbitrage Opportunities)

#### Triangular Currency Combinations (G10)
These form the basis for classic triangular arbitrage detection:

```
Triangle 1:  USD → EUR → GBP → USD    (Most liquid)
Triangle 2:  USD → EUR → JPY → USD    (High volume)
Triangle 3:  USD → GBP → JPY → USD    (Cable-Yen)
Triangle 4:  USD → EUR → CHF → USD    (SNB sensitivity)
Triangle 5:  USD → AUD → JPY → USD    (Carry trade triangle)
Triangle 6:  EUR → GBP → CHF → EUR    (European triangle)
Triangle 7:  USD → CAD → JPY → USD    (Oil-carry triangle)
Triangle 8:  USD → AUD → NZD → USD    (Antipodean triangle)
Triangle 9:  EUR → NOK → SEK → EUR    (Scandinavian triangle)
Triangle 10: USD → MXN → CAD → USD    (USMCA triangle)
```

#### Emerging Market Triangles (Higher Opportunity, Higher Risk)
```
Triangle 11: USD → EUR → PLN → USD    (EU convergence)
Triangle 12: USD → EUR → TRY → USD    (High volatility)
Triangle 13: USD → JPY → KRW → USD    (Asian tech)
Triangle 14: USD → CNH → HKD → USD    (Greater China)
Triangle 15: USD → BRL → MXN → USD    (LatAm)
Triangle 16: USD → ZAR → EUR → USD    (SA mining flows)
```

#### Gold Cross-Currency Arbitrage
Gold priced in different currencies should maintain parity via FX rates:

```
XAU/USD vs XAU/EUR × EUR/USD    (Primary check)
XAU/USD vs XAU/GBP × GBP/USD    (London fixing)
XAU/USD vs XAU/JPY × JPY/USD    (Asian session)
XAU/USD vs XAU/CHF × CHF/USD    (Swiss safe haven)
XAU/USD vs XAU/CNH × CNH/USD    (Shanghai premium)
XAU/USD vs XAU/INR × INR/USD    (India wedding season)
XAU/USD vs XAU/AED × AED/USD    (Dubai flows)
```

#### Direct Spread Arbitrage (Same Asset, Different Markets)
```
CNY vs CNH          (Onshore vs offshore yuan - KEY OPPORTUNITY)
ARS Blue vs Official (Argentina parallel rates - when accessible)
NDF vs Spot         (INR, KRW, TWD, BRL non-deliverable forwards)
COMEX vs LBMA Gold  (US vs London gold)
WTI vs Brent        (US vs global oil benchmark)
Henry Hub vs TTF    (US vs EU natural gas)
TTF vs JKM          (EU vs Asia LNG)
```

### 2.2 Tier 2: Precious Metals Ratio Analysis

| Ratio | Historical Range | Current Normal | Significance | Alert Levels |
|-------|------------------|----------------|--------------|--------------|
| **Gold/Silver** | 40:1 to 100:1 | ~65:1 | Mean reversion, monetary vs industrial | <50 or >85 |
| **Gold/Platinum** | 0.8:1 to 2.5:1 | ~1.8:1 | Platinum historically premium, now inverted | <1.0 or >2.2 |
| **Platinum/Palladium** | 0.3:1 to 5:1 | ~0.5:1 | Auto catalyst substitution | <0.4 or >1.5 |
| **Gold/Copper** (oz/lb) | 400:1 to 600:1 | ~500:1 | Risk-on vs risk-off indicator | <420 or >580 |
| **Silver/Copper** | 5:1 to 15:1 | ~10:1 | Industrial metals comparison | <6 or >14 |

### 2.3 Tier 3: Energy Spread Analysis (High Value Arbitrage)

| Spread | Historical Range | Drivers | Why It Matters |
|--------|------------------|---------|----------------|
| **WTI-Brent** | -$30 to +$5 | US production, export capacity | **Most traded energy arb** |
| **Brent-Dubai** | $0 to $5 | Asian demand, sour/sweet | Middle East flows |
| **Henry Hub-TTF** | -$5 to $30 | LNG shipping, seasonality | **Atlantic basin LNG arb** |
| **TTF-JKM** | -$2 to $15 | Asian premium, shipping | Pacific LNG flows |
| **Crack Spread** (3-2-1) | $5 to $40 | Refinery margins | Gasoline/heating oil vs crude |
| **Spark Spread** | Variable | Gas-to-power economics | Power generation arbitrage |
| **Frac Spread** | Variable | Ethane vs natural gas | Petrochemical arbitrage |

### 2.4 Tier 4: Agricultural Spread Analysis

| Spread | Description | Drivers | Seasonality |
|--------|-------------|---------|-------------|
| **CBOT-MATIF Wheat** | US vs EU wheat | Black Sea, quality | Harvest timing |
| **Corn-Wheat** | Feed substitution | Livestock demand | Q4 feed demand |
| **Soybean Crush** | Beans vs oil+meal | Crushing margins | S. American harvest |
| **Arabica-Robusta** | Quality premium | Vietnam vs Brazil | Frost season |
| **Sugar-Ethanol** | Brazil parity | Fuel prices, harvest | Brazil crush season |
| **Corn-Ethanol** | US biofuel parity | Mandates, gasoline | Summer driving |

### 2.5 Tier 5: Commodity-Currency Correlations (Statistical Arbitrage)

#### High Correlation Pairs (>0.7 historically)
```
AUD/USD ↔ Copper        (R² ~ 0.75) - Australia #1 exporter
AUD/USD ↔ Iron Ore      (R² ~ 0.70) - Pilbara exports
CAD/USD ↔ WTI Crude     (R² ~ 0.72) - Alberta oil sands
NOK/USD ↔ Brent Crude   (R² ~ 0.78) - North Sea production
BRL/USD ↔ Iron Ore      (R² ~ 0.65) - Vale exports
BRL/USD ↔ Soybeans      (R² ~ 0.62) - Cerrado production
BRL/USD ↔ Coffee        (R² ~ 0.58) - Minas Gerais
CLP/USD ↔ Copper        (R² ~ 0.80) - Escondida/Codelco
ZAR/USD ↔ Gold          (R² ~ 0.55) - Witwatersrand
ZAR/USD ↔ Platinum      (R² ~ 0.68) - Bushveld Complex
MYR/USD ↔ Palm Oil      (R² ~ 0.60) - Plantation exports
IDR/USD ↔ Palm Oil      (R² ~ 0.55) - Indonesian plantations
IDR/USD ↔ Nickel        (R² ~ 0.52) - Sulawesi processing
RUB/USD ↔ Brent         (R² ~ 0.75) - When tradeable
COP/USD ↔ Brent         (R² ~ 0.65) - Ecopetrol
GHS/USD ↔ Cocoa         (R² ~ 0.50) - West African production
```

#### Medium Correlation Pairs (0.4-0.7) - Regime Dependent
```
MXN/USD ↔ WTI           (R² ~ 0.45) - Pemex, but diversified
PEN/USD ↔ Copper        (R² ~ 0.55) - Antamina, Las Bambas
KRW/USD ↔ Semiconductors (R² ~ 0.50) - Samsung, SK Hynix
TWD/USD ↔ Semiconductors (R² ~ 0.55) - TSMC dominance
THB/USD ↔ Rice          (R² ~ 0.35) - World's largest exporter
```

### 2.6 Tier 6: Pegged Currency Stress Trades

| Currency | Peg | Stress Trade | Indicators to Watch |
|----------|-----|--------------|---------------------|
| **HKD** | 7.75-7.85/USD | Trade at band edges | HIBOR vs SOFR, China outflows |
| **DKK** | 7.46/EUR ±2.25% | Very tight band | DNB intervention, reserves |
| **SAR** | 3.75/USD | Oil stress test | Forward points, CDS |
| **AED** | 3.6725/USD | Diversification play | Real estate, tourism |
| **CNY** | PBOC fixing | Fixing vs market | Basket deviation, reserves |

### 2.7 Tier 7: Carry Trade Matrix

| Funding CCY | Target CCY | Typical Carry | Risk Factors |
|-------------|------------|---------------|--------------|
| JPY (0.25%) | MXN (11%) | ~10.75% | AMLO policy, US recession |
| JPY (0.25%) | BRL (13%) | ~12.75% | Lula policy, commodity cycle |
| JPY (0.25%) | ZAR (8%) | ~7.75% | Load shedding, politics |
| JPY (0.25%) | TRY (45%) | ~44.75% | **Extreme risk, policy chaos** |
| CHF (1.5%) | HUF (13%) | ~11.5% | EU tensions, Orban |
| EUR (4%) | PLN (6%) | ~2% | EU funds, convergence |
| USD (5%) | IDR (6%) | ~1% | Low carry, commodity upside |

### 2.8 Tier 8: Cross-Market Basis Trades

| Asset | Market A | Market B | Typical Basis | Opportunity |
|-------|----------|----------|---------------|-------------|
| Gold | COMEX | LBMA | 0-50 bps | Physical delivery arb |
| Gold | Shanghai | COMEX | 0-200 bps | **Shanghai premium** |
| Silver | COMEX | LBMA | 0-30 bps | Lower liquidity |
| Copper | COMEX | LME | Variable | **US vs global demand** |
| Copper | LME | Shanghai | Variable | China import arb |
| Oil | WTI | Brent | -$5 to +$5 | **Most liquid energy arb** |
| Nat Gas | Henry Hub | TTF | $5 to $30 | LNG shipping costs |
| Bitcoin | Coinbase | Binance | 0-100 bps | Exchange spread arb |
| Bitcoin | Spot | Futures | -5% to +20% | **Cash and carry** |

### 2.9 Tier 9: Seasonal Patterns (Calendar Arbitrage)

| Asset | Season | Pattern | Trade Window |
|-------|--------|---------|--------------|
| Natural Gas | Winter | Heating demand spike | Oct-Feb |
| Gold (INR) | Q4 | Diwali/wedding season | Sep-Nov |
| Soybeans | Harvest | S. American pressure | Mar-May |
| Coffee | Frost | Brazil frost fear | Jun-Aug |
| Gasoline | Summer | Driving season | Apr-Aug |
| Cocoa | Harvest | W. African main crop | Oct-Mar |
| JPY | Fiscal year-end | Repatriation flows | Mar |
| USD | Tax season | Repatriation | Apr |

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
| BRL/USD | 1.2% | 3.5% | 8.2% | 15.5% | EM Normal |
| TRY/USD | 2.5% | 6.8% | 15.2% | 28.4% | EM Extreme |

### 3.9 Energy Spread Dashboard

**Purpose**: Track key energy arbitrage opportunities in real-time

```
┌─────────────────────────────────────────────────────────────────┐
│                    ENERGY SPREAD MONITOR                        │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  WTI-BRENT SPREAD           HENRY HUB-TTF SPREAD               │
│  ┌─────────────────┐        ┌─────────────────┐                │
│  │    -$2.45       │        │    +$12.30      │                │
│  │   ▼ Contango    │        │   ▲ US Discount │                │
│  │ 30D Avg: -$2.10 │        │ 30D Avg: $15.20 │                │
│  │ Signal: NEUTRAL │        │ Signal: NARROW  │                │
│  └─────────────────┘        └─────────────────┘                │
│                                                                 │
│  3-2-1 CRACK SPREAD         COAL-GAS SWITCHING                 │
│  ┌─────────────────┐        ┌─────────────────┐                │
│  │    $28.50/bbl   │        │   Gas Favored   │                │
│  │   ▲ Strong      │        │   Switch: $45   │                │
│  │ Seasonal: HIGH  │        │   Current: $38  │                │
│  └─────────────────┘        └─────────────────┘                │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 3.10 Emerging Market Stress Monitor

**Purpose**: Track EM currency stress and arbitrage opportunities

```
┌──────────────────────────────────────────────────────────────────┐
│               EMERGING MARKET STRESS DASHBOARD                   │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  CURRENCY    SPOT     1M FWD   NDF SPREAD  STRESS   CARRY       │
│  ─────────────────────────────────────────────────────────────── │
│  USD/CNY    7.2450   7.2680    +32 bps    🟢 Low    2.1%        │
│  USD/CNH    7.2520   7.2750    +38 bps    🟡 Med    2.0%        │
│  CNY-CNH    -0.0070            -6 bps     🟡 WATCH              │
│  ─────────────────────────────────────────────────────────────── │
│  USD/INR    83.25    83.85     +72 bps    🟢 Low    4.2%        │
│  USD/KRW    1,328    1,335     +52 bps    🟢 Low    1.8%        │
│  USD/BRL    4.92     5.08      +325 bps   🟡 Med    8.5%        │
│  USD/MXN    17.15    17.42     +158 bps   🟢 Low    6.2%        │
│  USD/ZAR    18.45    18.92     +255 bps   🟡 Med    5.1%        │
│  USD/TRY    32.50    38.20     +1754 bps  🔴 HIGH   38.5%       │
│  ─────────────────────────────────────────────────────────────── │
│                                                                  │
│  PEGGED CURRENCIES                                               │
│  USD/HKD    7.8245   [Band: 7.75-7.85]    🟢 Mid-band           │
│  USD/SAR    3.7505   [Peg: 3.75]          🟢 Stable             │
│  EUR/DKK    7.4585   [Peg: 7.46 ±2.25%]   🟢 On-peg             │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

### 3.11 Commodity-Currency Correlation Matrix

**Purpose**: Identify divergences between commodities and correlated currencies

```
┌──────────────────────────────────────────────────────────────────┐
│            COMMODITY-CURRENCY DIVERGENCE MONITOR                 │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  PAIR              30D CORR   CURRENT   EXPECTED   DIVERGENCE   │
│  ────────────────────────────────────────────────────────────    │
│  Copper vs AUD      0.78      0.6520    0.6580     -0.9% 🟡     │
│  WTI vs CAD         0.72      1.3580    1.3520     +0.4% ⚪     │
│  Brent vs NOK       0.75      10.85     10.72      +1.2% 🟡     │
│  Iron Ore vs BRL    0.68      4.92      5.15       -4.5% 🟢     │
│  Copper vs CLP      0.82      925       918        +0.8% ⚪     │
│  Gold vs ZAR        0.55      18.45     18.90      -2.4% 🟡     │
│  Palm Oil vs MYR    0.62      4.72      4.68       +0.9% ⚪     │
│  Soybeans vs BRL    0.65      4.92      4.88       +0.8% ⚪     │
│                                                                  │
│  🟢 = Trade Signal (>3% divergence)                             │
│  🟡 = Watch (1-3% divergence)                                   │
│  ⚪ = No Signal (<1% divergence)                                │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

### 3.12 Carry Trade Optimizer

**Purpose**: Find optimal carry trades adjusted for volatility

```
┌──────────────────────────────────────────────────────────────────┐
│                   CARRY TRADE OPTIMIZER                          │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  FUNDING → TARGET    CARRY   3M VOL   SHARPE*   SIGNAL          │
│  ─────────────────────────────────────────────────────────────── │
│  JPY → MXN          10.2%    11.5%    0.89      🟢 STRONG       │
│  JPY → BRL          12.5%    16.2%    0.77      🟢 GOOD         │
│  CHF → PLN           4.2%     8.5%    0.49      🟡 MODERATE     │
│  JPY → ZAR           7.5%    15.8%    0.47      🟡 MODERATE     │
│  EUR → HUF           9.0%    12.4%    0.73      🟢 GOOD         │
│  JPY → TRY          42.0%    32.5%    1.29      ⚠️  HIGH RISK   │
│  JPY → IDR           5.8%     9.2%    0.63      🟢 GOOD         │
│                                                                  │
│  *Carry/Volatility ratio (higher = better risk-adjusted)        │
│                                                                  │
│  WARNING: TRY carry attractive but tail risk extreme            │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

### 3.13 Agricultural Seasonality Calendar

**Purpose**: Track seasonal patterns and spread opportunities

```
┌──────────────────────────────────────────────────────────────────┐
│              AGRICULTURAL SEASONALITY CALENDAR                   │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  COMMODITY    J  F  M  A  M  J  J  A  S  O  N  D   CURRENT      │
│  ────────────────────────────────────────────────────────────    │
│  Soybeans    ░░░▓▓▓▓▓░░░░░░░░░░░░░░░░▓▓░░        SAm Harvest    │
│  Corn        ░░░░░░░░▓▓▓▓░░░░░░░░░░░░░░░░        US Planting    │
│  Wheat       ░░░░░░▓▓▓▓▓░░░░░░░░░░░░░░░░░        N.Hem Harvest  │
│  Coffee      ░░░░░░▓▓▓▓▓▓░░░░░░░░░░░░░░░░        Brazil Frost   │
│  Sugar       ░░░▓▓▓▓▓▓▓▓▓▓░░░░░░░░░░░░░░░        Brazil Crush   │
│  Cocoa       ░░░░░░░░░░░░░░░░░░░░▓▓▓▓▓▓▓▓        WAf Main Crop  │
│  Cotton      ░░░░░▓▓▓▓▓▓░░░░░░░░░░░░░░░░░        US Planting    │
│  Palm Oil    ░░░░░░░░░░░░▓▓▓▓▓▓░░░░░░░░░░        Low Prod Szn   │
│                                                                  │
│  ▓ = High Volatility Period   ░ = Normal Period                 │
│  Current Month: JANUARY (marked with *)                         │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

### 3.14 Precious Metals Cross-Market Basis

**Purpose**: Track same-metal arbitrage across global exchanges

```
┌──────────────────────────────────────────────────────────────────┐
│              PRECIOUS METALS CROSS-MARKET BASIS                  │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  GOLD (XAU)                                                      │
│  ────────────────────────────────────────────────────────────    │
│  COMEX Spot:        $2,015.50                                   │
│  LBMA AM Fix:       $2,014.80    Basis: -$0.70  (-3.5 bps) ⚪   │
│  Shanghai (SGE):    $2,028.40    Basis: +$12.90 (+64 bps) 🟢    │
│  Tokyo (TOCOM):     $2,016.20    Basis: +$0.70  (+3.5 bps) ⚪   │
│  Dubai:             $2,017.80    Basis: +$2.30  (+11 bps) ⚪    │
│                                                                  │
│  SILVER (XAG)                                                    │
│  ────────────────────────────────────────────────────────────    │
│  COMEX Spot:        $23.45                                      │
│  LBMA Fix:          $23.42       Basis: -$0.03  (-13 bps) ⚪    │
│  Shanghai:          $23.85       Basis: +$0.40  (+170 bps) 🟢   │
│                                                                  │
│  ALERT: Shanghai Gold Premium elevated - China import demand    │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

### 3.15 Multi-Leg Arbitrage Path Finder

**Purpose**: Discover complex arbitrage paths across 4+ assets

```
┌──────────────────────────────────────────────────────────────────┐
│              MULTI-LEG ARBITRAGE PATH FINDER                     │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ACTIVE OPPORTUNITIES (Net profit after costs)                   │
│                                                                  │
│  4-LEG PATHS:                                                    │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │ USD → XAU → EUR → GBP → USD                                 │ │
│  │ Legs: Buy gold, Sell gold/EUR, Sell EUR/GBP, Sell GBP/USD   │ │
│  │ Gross: +4.2 bps | Costs: -2.8 bps | Net: +1.4 bps 🟢       │ │
│  └─────────────────────────────────────────────────────────────┘ │
│                                                                  │
│  COMMODITY-CURRENCY PATHS:                                       │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │ USD → Copper → AUD → JPY → USD                              │ │
│  │ Long copper, Short AUD (undervalued), Carry via JPY         │ │
│  │ Expected: +8.5 bps over 1 week | Risk: Medium               │ │
│  └─────────────────────────────────────────────────────────────┘ │
│                                                                  │
│  ENERGY-CURRENCY PATHS:                                          │
│  ┌─────────────────────────────────────────────────────────────┐ │
│  │ USD → WTI → CAD → USD (vs Brent → NOK → USD)                │ │
│  │ WTI/Brent spread + CAD/NOK divergence                       │ │
│  │ Expected: +5.2 bps | Convergence time: 3-5 days             │ │
│  └─────────────────────────────────────────────────────────────┘ │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

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

### 5.1 Real-Time Data Feeds - G10 Currencies

| Data Type | Source Options | Update Frequency | Cost Tier |
|-----------|---------------|------------------|-----------|
| FX Spot (G10) | Reuters Refinitiv, Bloomberg, OANDA, FXCM | Tick/100ms | $$$ |
| FX Forwards | Reuters, Bloomberg | 1s | $$$ |
| FX Options Vol | Reuters, Bloomberg, SuperDerivatives | 1s | $$$$ |

### 5.2 Real-Time Data Feeds - Emerging Markets

| Data Type | Source Options | Update Frequency | Notes |
|-----------|---------------|------------------|-------|
| EM FX Spot | Reuters, Bloomberg, local banks | 100ms-1s | Wider spreads |
| NDF Rates | Reuters, Bloomberg, EMTA | 1s | INR, KRW, TWD, BRL, CLP |
| CNY/CNH | Reuters, Bloomberg, HKEX | Tick | **Track spread!** |
| EM Forwards | Local banks, Reuters | 1s | Check liquidity |

### 5.3 Precious Metals Data

| Data Type | Source Options | Update Frequency | Notes |
|-----------|---------------|------------------|-------|
| COMEX Gold/Silver | CME Group | Tick | US session primary |
| LBMA Fixes | LBMA, ICE | 2x daily | AM/PM fix |
| Shanghai Gold (SGE) | SGE, Reuters | Tick | **Shanghai premium** |
| TOCOM | JPX | Tick | Yen-denominated |
| Platinum/Palladium | NYMEX, LPPM | Tick | Auto catalyst focus |
| Kitco/Metals Focus | Kitco API | 1s | Aggregated spot |

### 5.4 Industrial Metals Data

| Data Type | Source Options | Update Frequency | Notes |
|-----------|---------------|------------------|-------|
| LME Base Metals | LME, Reuters | Tick | Cu, Al, Zn, Ni, Pb, Sn |
| COMEX Copper | CME Group | Tick | US benchmark |
| Shanghai Futures (SHFE) | SHFE | Tick | **China premium** |
| Iron Ore (SGX) | SGX | Tick | Physical benchmark |
| Iron Ore (DCE) | Dalian | Tick | China domestic |

### 5.5 Energy Data

| Data Type | Source Options | Update Frequency | Notes |
|-----------|---------------|------------------|-------|
| WTI Crude | NYMEX/CME | Tick | **WTI/Brent spread** |
| Brent Crude | ICE | Tick | Global benchmark |
| Natural Gas (HH) | NYMEX | Tick | US benchmark |
| Natural Gas (TTF) | ICE Endex | Tick | EU benchmark |
| JKM LNG | CME/Platts | Daily | Asia spot LNG |
| Coal | ICE, SGX | Daily | Newcastle, API2 |
| Power | Various ISOs | Hourly | Regional prices |
| Carbon (EUA) | ICE | Tick | EU ETS |

### 5.6 Agricultural Data

| Data Type | Source Options | Update Frequency | Notes |
|-----------|---------------|------------------|-------|
| Grains (CBOT) | CME Group | Tick | Wheat, Corn, Soybeans |
| Softs (ICE) | ICE | Tick | Coffee, Cocoa, Sugar, Cotton |
| MATIF Grains | Euronext | Tick | EU wheat/corn |
| Palm Oil (BMD) | Bursa Malaysia | Tick | MYR-denominated |
| Rice | CBOT, Thailand | Daily | Thin liquidity |
| Livestock | CME | Tick | Cattle, Hogs |

### 5.7 Alternative/Strategic Metals

| Data Type | Source Options | Update Frequency | Notes |
|-----------|---------------|------------------|-------|
| Lithium | Fastmarkets, Asian Metal | Weekly | Spot/contract |
| Cobalt | LME, Fastmarkets | Daily | DRC concentration |
| Rare Earths | Asian Metal, SMM | Weekly | China-dominated |
| Uranium | UxC, Numerco | Weekly | Spot/term |

### 5.8 Aggregated/Multi-Asset Platforms

| Platform | Coverage | Strengths |
|----------|----------|-----------|
| Bloomberg Terminal | Everything | Gold standard, expensive |
| Reuters Refinitiv | Everything | Strong FX, news |
| TradingView | Broad retail | Good charting, limited API |
| Quandl/Nasdaq Data Link | Historical focus | Clean datasets |
| Alpha Vantage | FX, Crypto, Stocks | Free tier available |
| OANDA | FX primary | Retail-friendly API |
| Polygon.io | FX, Crypto | Developer-friendly |
| IEX Cloud | Broad | Good API, reasonable cost |

### 5.9 FREE Data Sources (Quality Tier Ranked)

#### Tier 1: Excellent Free Sources (Production Quality)

| Source | Asset Classes | API | Rate Limit | Quality |
|--------|---------------|-----|------------|---------|
| **Yahoo Finance** (yfinance) | FX, Metals, Commodities, Crypto | Python lib | ~2000/hr | ⭐⭐⭐⭐ |
| **FRED (St. Louis Fed)** | FX rates, interest rates, economic | REST | Unlimited | ⭐⭐⭐⭐⭐ |
| **ECB Data Portal** | EUR crosses, official rates | REST/SDMX | Unlimited | ⭐⭐⭐⭐⭐ |
| **Bank of England** | GBP rates, historical | REST | Unlimited | ⭐⭐⭐⭐⭐ |
| **Exchangerate.host** | 170+ FX pairs | REST | 1000/mo free | ⭐⭐⭐⭐ |
| **Open Exchange Rates** | FX rates | REST | 1000/mo free | ⭐⭐⭐⭐ |

#### Tier 2: Good Free Sources (Development/Research)

| Source | Asset Classes | Update Freq | Notes |
|--------|---------------|-------------|-------|
| **Alpha Vantage** | FX, Crypto, Stocks | 5/min, 500/day | Good for prototyping |
| **CoinGecko** | Crypto only | 10-50/min | Excellent crypto coverage |
| **CoinMarketCap** | Crypto only | 333/day free | Market cap focus |
| **Metals-API** | Precious metals | 50/mo free | Gold, Silver, Platinum |
| **GoldAPI.io** | Precious metals | 300/mo free | Real-time gold |
| **Twelve Data** | FX, Stocks, Crypto | 800/day free | Good documentation |

#### Tier 3: Government & Central Bank Sources (Best for EM)

| Source | Coverage | Update | API |
|--------|----------|--------|-----|
| **PBOC** (China) | CNY fixing, rates | Daily | Web scrape |
| **RBI** (India) | INR reference rates | Daily | Web scrape |
| **BCB** (Brazil) | BRL rates, PTAX | Daily | REST API |
| **Banxico** (Mexico) | MXN rates | Daily | REST API |
| **SARB** (South Africa) | ZAR rates | Daily | Web scrape |
| **BOJ** (Japan) | JPY rates | Daily | REST |
| **BIS** | Cross-border flows | Monthly | REST/CSV |

#### Tier 4: Commodity-Specific Free Sources

| Source | Commodities | Update | Format |
|--------|-------------|--------|--------|
| **EIA.gov** | Oil, Gas, Coal, Uranium | Weekly/Daily | REST API |
| **USDA** | All agricultural | Weekly | REST/FTP |
| **LME** (delayed) | Base metals | 15-min delay | Web |
| **Kitco** (delayed) | Precious metals | 15-min delay | Web scrape |
| **Investing.com** | Everything | Real-time | Web scrape |
| **Trading Economics** | Everything | Daily | Web scrape |

#### Detailed Free Source Specifications

**Yahoo Finance (via yfinance Python library)**
```python
# Best free source for multi-asset coverage
import yfinance as yf

# FX rates
eurusd = yf.Ticker("EURUSD=X")
gbpjpy = yf.Ticker("GBPJPY=X")

# Precious metals
gold = yf.Ticker("GC=F")      # Gold futures
silver = yf.Ticker("SI=F")    # Silver futures

# Energy
wti = yf.Ticker("CL=F")       # WTI crude
brent = yf.Ticker("BZ=F")     # Brent crude
natgas = yf.Ticker("NG=F")    # Natural gas

# Agricultural
corn = yf.Ticker("ZC=F")
wheat = yf.Ticker("ZW=F")
soybeans = yf.Ticker("ZS=F")
coffee = yf.Ticker("KC=F")

# EM currencies
usdbrl = yf.Ticker("BRL=X")
usdmxn = yf.Ticker("MXN=X")
usdzar = yf.Ticker("ZAR=X")
usdtry = yf.Ticker("TRY=X")
usdcny = yf.Ticker("CNY=X")
```

**FRED (Federal Reserve Economic Data)**
```
https://api.stlouisfed.org/fred/series/observations

Key Series IDs:
- DEXUSEU: USD/EUR daily
- DEXJPUS: JPY/USD daily
- DEXCHUS: CNY/USD daily
- DEXBZUS: BRL/USD daily
- GOLDAMGBD228NLBM: London gold fixing
- DCOILWTICO: WTI crude spot
- DCOILBRENTEU: Brent crude spot
- DHHNGSP: Henry Hub natural gas
- PCOFFOTMUSDM: Coffee price
- PCOALAUUSDM: Coal price

Rate limit: None (with free API key)
History: 50+ years for many series
```

**ECB Statistical Data Warehouse**
```
https://sdw-wsrest.ecb.europa.eu/service/data/

Excellent for:
- EUR crosses (official ECB rates)
- Euro area interest rates
- Historical data back to 1999

Example: EUR/USD daily
https://sdw-wsrest.ecb.europa.eu/service/data/EXR/D.USD.EUR.SP00.A
```

**Open Exchange Rates / Exchangerate.host**
```
# Free tier: 1000 requests/month
https://api.exchangerate.host/latest?base=USD

# Historical rates
https://api.exchangerate.host/2024-01-15?base=USD

Coverage: 170+ currencies including:
- All G10
- Most EM (BRL, MXN, ZAR, TRY, INR, etc.)
- Crypto (BTC, ETH)
```

**EIA (Energy Information Administration)**
```
https://api.eia.gov/v2/

Free API key required
Excellent coverage:
- WTI/Brent spot and futures
- Natural gas (Henry Hub, regional)
- Petroleum products
- Coal prices
- Uranium prices
- Storage/inventory data

Weekly petroleum status report: Key for energy arb
```

**USDA (Agricultural Data)**
```
https://quickstats.nass.usda.gov/api

Coverage:
- All major grains (corn, wheat, soybeans)
- Livestock
- Dairy
- Production, stocks, exports

Also: WASDE reports for supply/demand
```

#### Free Source Limitations & Workarounds

| Limitation | Impact | Workaround |
|------------|--------|------------|
| 15-min delay | Missed fast arb | Combine multiple sources |
| Rate limits | Gaps in data | Cache aggressively, batch requests |
| No tick data | Can't detect micro-arb | Focus on statistical arb (longer hold) |
| Weekend gaps | FX gap risk | Use crypto as proxy for weekend sentiment |
| EM coverage | Limited CNH, NDF | Use central bank sources directly |

#### Recommended Free Stack for MVP

**For FX Arbitrage:**
1. Yahoo Finance (yfinance) - Primary real-time
2. FRED - Historical backfill
3. ECB - EUR cross validation
4. Central banks - EM official rates

**For Commodity-Currency Correlation:**
1. Yahoo Finance - Commodity futures
2. EIA - Energy official data
3. USDA - Agricultural data
4. FRED - Historical prices

**For Precious Metals:**
1. Yahoo Finance - Futures prices
2. FRED - LBMA fixing
3. GoldAPI.io - Real-time spot
4. Kitco (scrape) - Multi-metal

**For Crypto Arbitrage:**
1. CoinGecko - Comprehensive, free
2. Binance API - Free, real-time
3. Coinbase API - Free, US prices
4. CoinMarketCap - Market data

#### Sample Data Pipeline (Free Sources)

```
┌─────────────────────────────────────────────────────────────┐
│                    FREE DATA PIPELINE                        │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌──────────────┐    ┌──────────────┐    ┌──────────────┐  │
│  │   yfinance   │    │     FRED     │    │  Central     │  │
│  │  (Real-time) │    │ (Historical) │    │   Banks      │  │
│  └──────┬───────┘    └──────┬───────┘    └──────┬───────┘  │
│         │                   │                   │           │
│         └─────────┬─────────┴─────────┬─────────┘           │
│                   ▼                   ▼                     │
│         ┌─────────────────────────────────────┐             │
│         │         DATA NORMALIZER              │             │
│         │  • Align timestamps                  │             │
│         │  • Handle missing data               │             │
│         │  • Convert units                     │             │
│         └─────────────────┬───────────────────┘             │
│                           ▼                                  │
│         ┌─────────────────────────────────────┐             │
│         │         LOCAL CACHE (SQLite)         │             │
│         │  • 1-min OHLCV for recent            │             │
│         │  • Daily for historical              │             │
│         └─────────────────┬───────────────────┘             │
│                           ▼                                  │
│         ┌─────────────────────────────────────┐             │
│         │       ARBITRAGE CALCULATOR           │             │
│         └─────────────────────────────────────┘             │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### 5.10 Historical Data

| Data Type | Granularity | History Depth | Sources |
|-----------|-------------|---------------|---------|
| FX OHLCV | Tick to Daily | 20+ years | Dukascopy, HistData, FXCM |
| Metals OHLCV | 1min to Daily | 15+ years | Quandl, CME DataMine |
| Energy OHLCV | 1min to Daily | 15+ years | CME, ICE, EIA |
| EM FX | Daily | 10+ years | Central banks, BIS |
| Agricultural | Daily | 30+ years | USDA, CME |

### 5.11 Derived/Calculated Data

**Core Calculations:**
- Implied cross rates from direct rates
- Rolling correlations (5D, 20D, 60D, 252D windows)
- Historical and implied volatility
- Ratio time series (Gold/Silver, etc.)
- Spread time series (WTI-Brent, etc.)
- Carry-adjusted returns
- Z-scores from rolling means

**Advanced Analytics:**
- Cointegration tests for pairs
- Half-life of mean reversion
- Regime detection (HMM models)
- Transaction cost estimates by pair
- Liquidity scores
- Stress test scenarios

### 5.12 Reference Data

| Data Type | Sources | Update Frequency |
|-----------|---------|------------------|
| Holiday calendars | Bloomberg, Reuters | Daily |
| Trading hours | Exchange websites | Periodic |
| Contract specs | Exchange websites | Periodic |
| Delivery locations | CME, LME specs | Periodic |
| Margin requirements | Brokers, exchanges | Daily |
| Transaction costs | Broker feeds | Daily |

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

## 12. Highest-Value Arbitrage Opportunities (Ranked)

Based on historical frequency, profitability, and executability, here are the most valuable opportunities to monitor:

### 12.1 Tier 1: Institutional-Grade Opportunities (High Frequency, Lower Margin)

| Rank | Opportunity | Avg Profit | Frequency | Execution Difficulty |
|------|-------------|------------|-----------|---------------------|
| 1 | **CNY/CNH Spread** | 5-50 bps | Daily | Medium - requires China access |
| 2 | **WTI/Brent Spread** | 10-100 bps | Continuous | Low - very liquid |
| 3 | **Gold COMEX/Shanghai** | 20-100 bps | Daily | Medium - China access |
| 4 | **G10 Triangular Arb** | 1-5 bps | Frequent | Low - need speed |
| 5 | **Copper LME/COMEX** | 10-50 bps | Daily | Low - liquid markets |

### 12.2 Tier 2: Statistical Arbitrage (Mean Reversion)

| Rank | Opportunity | Signal Quality | Avg Hold Time | Annual Sharpe |
|------|-------------|----------------|---------------|---------------|
| 1 | **Gold/Silver Ratio** | High | 2-8 weeks | ~0.8 |
| 2 | **AUD vs Copper** | High | 1-4 weeks | ~0.7 |
| 3 | **BRL vs Iron Ore** | Medium | 1-3 weeks | ~0.6 |
| 4 | **CAD vs WTI** | High | 1-2 weeks | ~0.7 |
| 5 | **NOK vs Brent** | High | 1-2 weeks | ~0.6 |
| 6 | **Gold/Platinum** | Medium | 4-12 weeks | ~0.5 |
| 7 | **CLP vs Copper** | Very High | 1-2 weeks | ~0.9 |

### 12.3 Tier 3: Event-Driven Opportunities

| Event Type | Currencies/Assets | Opportunity | Alert Trigger |
|------------|-------------------|-------------|---------------|
| PBOC Fixing | CNY/CNH | Fixing vs market gap | Daily 9:15 Beijing |
| LBMA Fix | Gold, Silver | Fix vs spot divergence | 10:30, 15:00 London |
| HKD Band Touch | HKD | HKMA intervention | 7.75 or 7.85 level |
| RBI Intervention | INR | NDF/spot spread | Large INR moves |
| Brazil BCB | BRL | FX intervention | Swap auctions |
| SNB Floor/Ceiling | CHF | Historic interventions | Crisis periods |
| Oil Inventory | WTI, Brent, CAD, NOK | EIA/API surprise | Wed 10:30 ET |

### 12.4 Tier 4: Carry Trade Arbitrage (Risk-Adjusted)

**Best Risk/Reward Carry Trades (2024-2026 Environment):**

| Trade | Carry | Vol | Sharpe | Key Risk |
|-------|-------|-----|--------|----------|
| JPY → MXN | 10.5% | 11% | 0.95 | Banxico policy |
| CHF → PLN | 4.5% | 8% | 0.56 | EU politics |
| EUR → HUF | 9.0% | 12% | 0.75 | Orban/EU |
| JPY → IDR | 5.5% | 9% | 0.61 | Commodity cycle |
| USD → BRL | 8.0% | 15% | 0.53 | Lula policy |

**Avoid (Negative Risk-Adjusted):**
| Trade | Carry | Vol | Sharpe | Why Avoid |
|-------|-------|-----|--------|-----------|
| JPY → TRY | 42% | 35% | 1.20 | Tail risk, policy chaos |
| JPY → ARS | 50%+ | 40%+ | N/A | Capital controls |

### 12.5 Tier 5: Seasonal/Calendar Arbitrage

| Month | Best Opportunities | Historical Win Rate |
|-------|-------------------|---------------------|
| January | JPY repatriation (long JPY) | 65% |
| March | Japan fiscal year-end (long JPY) | 70% |
| April | US tax repatriation (long USD) | 60% |
| June-Aug | Coffee frost premium (long KC) | 55% |
| September | Gold Diwali demand (long XAU/INR) | 68% |
| October | Heating oil build (HO/CL spread) | 62% |
| December | Year-end USD squeeze | 58% |

### 12.6 Tier 6: Cross-Market Basis (Physical Arbitrage)

| Asset | Markets | Typical Basis | Logistics |
|-------|---------|---------------|-----------|
| Gold | COMEX → London | 0-10 bps | Air freight |
| Gold | London → Shanghai | 20-100 bps | Regulated import |
| Copper | LME → COMEX | 10-50 bps | Shipping |
| Copper | LME → Shanghai | Variable | China import |
| Oil | Cushing → Gulf | Variable | Pipeline |
| LNG | US → Europe | $2-5/mmBtu | Tanker charter |
| LNG | US → Asia | $3-8/mmBtu | Long voyage |

---

## 13. Risk Management Framework

### 13.1 Position Sizing by Opportunity Type

| Opportunity Type | Max Position | Stop Loss | Take Profit |
|------------------|--------------|-----------|-------------|
| Triangular FX Arb | 5% of book | 2 bps | 3+ bps |
| Statistical Arb | 10% of book | 2σ move | Mean reversion |
| Carry Trade | 15% of book | 5% adverse | Roll monthly |
| Event-Driven | 3% of book | 1% adverse | 2x expected |
| Commodity-FX | 8% of book | 3% adverse | Correlation restore |

### 13.2 Correlation Monitoring

Monitor for correlation breakdown - key warning signs:
- 20D correlation drops below 60D correlation by >0.2
- Z-score of spread exceeds 3σ
- Implied vol spikes above realized vol

### 13.3 Liquidity Thresholds

| Asset Class | Min Daily Volume | Max Spread | Max Position % |
|-------------|------------------|------------|----------------|
| G10 FX | $1B | 3 pips | 0.1% of ADV |
| EM FX | $100M | 20 pips | 0.05% of ADV |
| Gold | $50M | $0.50 | 0.1% of ADV |
| Copper | $20M | $5 | 0.1% of ADV |
| Ags | $10M | 0.5% | 0.05% of ADV |

---

## 14. Appendix: Arbitrage Formulas

### A. Triangular Arbitrage
```
Given currencies A, B, C:
Profit = (1/Rate_AB) × Rate_BC × Rate_CA - 1

Example: USD → EUR → GBP → USD
If EUR/USD = 1.08, GBP/EUR = 0.85, USD/GBP = 1.27
Profit = (1/1.08) × 0.85 × 1.27 - 1 = 0.00% (no arbitrage)

With transaction costs:
Net_Profit = Gross_Profit - (Spread_AB + Spread_BC + Spread_CA)
Execute only if Net_Profit > Minimum_Threshold (typically 1-2 bps)
```

### B. Cross-Rate Parity
```
Implied Cross Rate = Rate_A/Base × Rate_Base/B
Discrepancy = |Quoted - Implied| / Quoted

Example: EUR/GBP
Implied = EUR/USD × USD/GBP = 1.08 × 0.787 = 0.850
If Quoted = 0.852, Discrepancy = 0.23%
```

### C. Precious Metals Parity
```
XAU/USD should equal XAU/EUR × EUR/USD
Spread = XAU/USD - (XAU/EUR × EUR/USD)

Shanghai Premium Calculation:
Shanghai_Premium = (SGE_Gold_Yuan / USDCNY) - COMEX_Gold_USD
Premium_Percent = Shanghai_Premium / COMEX_Gold_USD × 100
```

### D. Energy Spread Calculations

**WTI-Brent Spread:**
```
Spread = WTI_Price - Brent_Price
Typically negative (Brent premium due to global benchmark status)
Historical range: -$30 to +$5

Trade signal:
If Spread < -$10: Consider long WTI / short Brent
If Spread > $0: Consider short WTI / long Brent
```

**Crack Spread (3-2-1):**
```
Crack_Spread = (2 × Gasoline_Price + 1 × Heating_Oil_Price) / 3 - Crude_Price
Result in $/barrel represents refining margin

Typical range: $5 to $40/bbl
Seasonality: Higher in summer (gasoline) and winter (heating oil)
```

**Natural Gas Basis (Henry Hub to TTF):**
```
LNG_Arb = TTF_Price - Henry_Hub_Price - Shipping_Cost - Liquefaction_Cost
Shipping_Cost ≈ $1.50-3.00/mmBtu (Atlantic route)
Liquefaction ≈ $2.00-3.00/mmBtu

If LNG_Arb > 0: Economic to ship US gas to Europe
```

### E. Commodity-Currency Correlation Divergence

**Z-Score Calculation:**
```
Expected_FX = α + β × Commodity_Price
Residual = Actual_FX - Expected_FX
Z_Score = Residual / Standard_Deviation(Residuals)

Trading Signal:
Z > +2: Currency overvalued vs commodity → Short currency
Z < -2: Currency undervalued vs commodity → Long currency
```

**Example: AUD vs Copper**
```
Regression: AUD/USD = 0.45 + 0.00005 × Copper_Price
If Copper = $4.00/lb ($8,800/mt):
Expected AUD = 0.45 + 0.00005 × 8800 = 0.89
If Actual AUD = 0.85:
Residual = 0.85 - 0.89 = -0.04
Z_Score = -0.04 / 0.02 = -2.0 → AUD undervalued
```

### F. Carry Trade Calculation

**Unhedged Carry Return:**
```
Carry_Return = (1 + Target_Rate) / (1 + Funding_Rate) - 1 + FX_Return

Annualized_Carry = Target_Rate - Funding_Rate
FX_Return = (Spot_End - Spot_Start) / Spot_Start

Total_Return = Annualized_Carry + FX_Return
```

**Risk-Adjusted Carry (Sharpe-like):**
```
Carry_Sharpe = Annualized_Carry / FX_Volatility

Example: JPY → MXN
Carry = 11% - 0.25% = 10.75%
MXN Volatility = 12%
Carry_Sharpe = 10.75% / 12% = 0.90 (attractive)
```

**Forward Points Arbitrage:**
```
Theoretical_Forward = Spot × (1 + Target_Rate) / (1 + Base_Rate)
Forward_Points = (Theoretical - Actual) / Spot × 10000

If Forward_Points deviation > Transaction_Costs:
→ Covered interest arbitrage opportunity
```

### G. Ratio Mean Reversion

**Gold/Silver Ratio:**
```
Ratio = Gold_Price / Silver_Price
Historical_Mean = 65:1 (approximate)
Current = 86:1

Z_Score = (Current - Mean) / Std_Dev
Half_Life = -ln(2) / ln(AR1_Coefficient)

Trade sizing:
Position_Size = Base_Size × min(|Z_Score| / 2, 1.5)
```

**Expected Profit:**
```
If Z = +2 (ratio high, silver cheap):
Expected_Reversion = 0.5 × (Current_Ratio - Mean_Ratio)
Expected_Return = Expected_Reversion / Current_Ratio

Trade: Long silver, Short gold (ratio hedge)
```

### H. Cross-Market Basis Arbitrage

**Physical Arbitrage Calculation:**
```
Arbitrage_Profit = Price_Market_B - Price_Market_A - Transport_Cost - Financing

Example: Gold COMEX to Shanghai
Shanghai_Price_USD = 2028
COMEX_Price = 2015
Transport = $2
Financing (1 week) = $1
Net_Arbitrage = 2028 - 2015 - 2 - 1 = $10/oz profit

Annualized = ($10 / $2015) × 52 = 25.8%
```

### I. NDF vs Spot Spread (Emerging Markets)

```
NDF_Implied_Rate = (NDF_Forward / Spot - 1) × (360 / Days) × 100
Onshore_Rate = Local interbank rate
Offshore_Rate = USD SOFR + Country_Risk_Premium

NDF_Spread = NDF_Implied_Rate - Onshore_Rate
If |NDF_Spread| > 100 bps: Significant stress indicator
```

### J. Pegged Currency Band Trading

**HKD Example:**
```
Band_Range = 7.85 - 7.75 = 0.10
Position_In_Band = (Current - 7.75) / 0.10

Trading Logic:
If Position > 0.9 (near weak side 7.85):
  → Expect HKMA intervention → Long HKD
If Position < 0.1 (near strong side 7.75):
  → HKMA may allow weakening → Neutral/Short HKD

HIBOR_Spike = HIBOR - SOFR
If HIBOR_Spike > 200 bps: Defense mode, intervention likely
```

---

## 16. TRADING EXECUTION MODULE

### 16.1 Account Parameters & Goals

**Starting Capital**: $100
**Target**: 2x account every 60 days (100% return)
**Required Daily Return**: ~1.16% compound
**Required Weekly Return**: ~8.4%
**Risk Tolerance**: Aggressive but controlled

```
Growth Trajectory:
Day 0:   $100.00
Day 15:  $118.87  (+18.9%)
Day 30:  $141.28  (+41.3%)
Day 45:  $167.91  (+67.9%)
Day 60:  $199.50  (+99.5%) ≈ $200 TARGET
Day 90:  $398.00  (4x)
Day 120: $795.00  (8x)
Day 180: $3,170   (32x)
Day 365: $63,400  (634x) - theoretical maximum
```

### 16.2 Strategy Selection for $100 Account

Given the small account size, we must focus on:
1. **Zero/low commission brokers**
2. **No minimum position sizes** (or very low)
3. **High leverage available** (carefully managed)
4. **Liquid markets** (tight spreads)

#### Optimal Strategies by Account Size

| Account Size | Best Strategies | Why |
|--------------|-----------------|-----|
| **$100-500** | Crypto arb, FX micro-lots, CFDs | No minimums, 24/7, high leverage |
| **$500-2000** | Add: Commodity CFDs, more FX pairs | Can diversify |
| **$2000-10000** | Add: Futures micro-contracts, options | Meet minimums |
| **$10000+** | Full strategy suite | Professional access |

#### Primary Strategies for $100 Account

**Strategy 1: Crypto Exchange Arbitrage (40% allocation)**
```
Capital Allocated: $40
Exchanges: Binance, Coinbase, Kraken, KuCoin
Target Pairs: BTC/USDT, ETH/USDT, SOL/USDT
Expected Spread: 10-50 bps during volatility
Trades/Day: 5-20
Expected Daily Return: 0.3-0.8%
```

**Strategy 2: Crypto Triangular Arbitrage (25% allocation)**
```
Capital Allocated: $25
Exchange: Single exchange (Binance preferred)
Triangles: BTC→ETH→USDT→BTC, BTC→SOL→USDT→BTC
Expected Spread: 5-20 bps
Trades/Day: 10-50
Expected Daily Return: 0.2-0.5%
```

**Strategy 3: FX Micro-Lot Trading (20% allocation)**
```
Capital Allocated: $20
Broker: OANDA, Forex.com (micro-lot support)
Pairs: EUR/USD, GBP/USD, USD/JPY
Strategy: Statistical arb on correlations
Leverage: 10:1 max
Expected Daily Return: 0.3-0.6%
```

**Strategy 4: Stablecoin Yield + Arbitrage (15% allocation)**
```
Capital Allocated: $15
Platforms: DeFi (Aave, Compound), CEX earn
Base Yield: 5-15% APY
Arb Opportunities: USDT/USDC/DAI spreads
Expected Daily Return: 0.1-0.3%
```

### 16.3 Broker & Exchange Integration

#### Crypto Exchanges (Primary - Best for $100)

| Exchange | API | Fees | Min Trade | Why Use |
|----------|-----|------|-----------|---------|
| **Binance** | REST + WebSocket | 0.1% (0.075% w/ BNB) | $1 | Best liquidity, most pairs |
| **Coinbase Pro** | REST + WebSocket | 0.5% maker/taker | $1 | US regulated, fiat on-ramp |
| **Kraken** | REST + WebSocket | 0.16%/0.26% | $1 | Good for EUR pairs |
| **KuCoin** | REST + WebSocket | 0.1% | $1 | Many altcoins, arb opportunities |
| **Bybit** | REST + WebSocket | 0.1% | $1 | Good derivatives |

**API Integration Code Structure:**
```python
# Unified exchange interface
class ExchangeAdapter:
    def __init__(self, exchange_name, api_key, secret):
        self.exchange = ccxt.exchange_name({
            'apiKey': api_key,
            'secret': secret,
            'enableRateLimit': True
        })

    def get_ticker(self, symbol):
        return self.exchange.fetch_ticker(symbol)

    def place_order(self, symbol, side, amount, price=None):
        if price:
            return self.exchange.create_limit_order(symbol, side, amount, price)
        return self.exchange.create_market_order(symbol, side, amount)

    def get_balance(self):
        return self.exchange.fetch_balance()
```

#### Forex Brokers (Secondary)

| Broker | API | Min Deposit | Min Lot | Leverage | Notes |
|--------|-----|-------------|---------|----------|-------|
| **OANDA** | REST v20 | $0 | 1 unit | 50:1 | Best for micro accounts |
| **Forex.com** | REST | $100 | 1K units | 50:1 | Good execution |
| **IG** | REST | $250 | Micro | 30:1 | CFDs available |

**OANDA API Example:**
```python
import oandapyV20
from oandapyV20.endpoints import orders, pricing

class ForexTrader:
    def __init__(self, account_id, access_token):
        self.client = oandapyV20.API(access_token=access_token)
        self.account_id = account_id

    def get_price(self, instrument):
        params = {"instruments": instrument}
        r = pricing.PricingInfo(self.account_id, params=params)
        return self.client.request(r)

    def market_order(self, instrument, units):
        data = {
            "order": {
                "type": "MARKET",
                "instrument": instrument,
                "units": str(units),
                "timeInForce": "FOK"
            }
        }
        r = orders.OrderCreate(self.account_id, data=data)
        return self.client.request(r)
```

### 16.4 Position Sizing for $100 Account

#### Kelly Criterion Adaptation

```
Optimal Position Size = (Win_Rate × Avg_Win - Loss_Rate × Avg_Loss) / Avg_Win

For arbitrage with:
- Win Rate: 85%
- Avg Win: 0.3%
- Avg Loss: 0.5%

Kelly = (0.85 × 0.003 - 0.15 × 0.005) / 0.003 = 0.60 (60%)

Half-Kelly (safer): 30% per trade
Quarter-Kelly (conservative): 15% per trade
```

#### Position Sizing Rules

| Strategy | Max Position | Max Leverage | Stop Loss | Reason |
|----------|-------------|--------------|-----------|--------|
| Crypto Spot Arb | 40% of capital | 1x | 1% | Need funds on 2 exchanges |
| Crypto Triangle | 25% of capital | 1x | 0.5% | Fast execution required |
| FX Micro | 20% of capital | 10x | 2% | Leverage amplifies |
| Stablecoin | 15% of capital | 1x | 0.1% | Very low risk |

#### Concurrent Position Limits

```
Maximum Open Positions: 4
Maximum Correlated Positions: 2
Maximum Single-Asset Exposure: 50%
Maximum Leverage (Portfolio): 5x effective
Minimum Cash Reserve: 10% ($10)
```

### 16.5 Automated Execution Engine

#### System Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                    ARBITRAGE TRADING ENGINE                          │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌──────────────────────────────────────────────────────────────┐   │
│  │                     SIGNAL GENERATOR                          │   │
│  │  • Price feeds from all exchanges                            │   │
│  │  • Arbitrage opportunity detection                           │   │
│  │  • Signal scoring and ranking                                │   │
│  └──────────────────────────────┬───────────────────────────────┘   │
│                                 │                                    │
│                                 ▼                                    │
│  ┌──────────────────────────────────────────────────────────────┐   │
│  │                    RISK MANAGER                               │   │
│  │  • Position sizing calculation                               │   │
│  │  • Exposure limits check                                     │   │
│  │  • Correlation analysis                                      │   │
│  │  • Stop-loss levels                                          │   │
│  └──────────────────────────────┬───────────────────────────────┘   │
│                                 │                                    │
│                    ┌────────────┴────────────┐                      │
│                    ▼                         ▼                       │
│  ┌─────────────────────────┐  ┌─────────────────────────────────┐   │
│  │   EXECUTION MANAGER     │  │      PORTFOLIO TRACKER          │   │
│  │  • Order routing        │  │  • P&L calculation              │   │
│  │  • Slippage control     │  │  • Position tracking            │   │
│  │  • Fill confirmation    │  │  • Performance metrics          │   │
│  │  • Retry logic          │  │  • Daily/weekly reports         │   │
│  └───────────┬─────────────┘  └─────────────────────────────────┘   │
│              │                                                       │
│              ▼                                                       │
│  ┌──────────────────────────────────────────────────────────────┐   │
│  │                    EXCHANGE ADAPTERS                          │   │
│  │  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐            │   │
│  │  │ Binance │ │Coinbase │ │  OANDA  │ │ Kraken  │            │   │
│  │  └─────────┘ └─────────┘ └─────────┘ └─────────┘            │   │
│  └──────────────────────────────────────────────────────────────┘   │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

#### Core Execution Logic

```python
class ArbitrageEngine:
    def __init__(self, config):
        self.exchanges = self._init_exchanges(config)
        self.risk_manager = RiskManager(config)
        self.portfolio = Portfolio(starting_capital=100)
        self.min_profit_threshold = 0.001  # 0.1% minimum

    async def run(self):
        while True:
            # 1. Fetch prices from all sources
            prices = await self._fetch_all_prices()

            # 2. Detect arbitrage opportunities
            opportunities = self._detect_arbitrage(prices)

            # 3. Filter by profitability (after fees)
            viable = [o for o in opportunities
                     if o.net_profit > self.min_profit_threshold]

            # 4. Rank by risk-adjusted return
            ranked = sorted(viable, key=lambda x: x.sharpe, reverse=True)

            # 5. Check risk limits
            for opp in ranked:
                if self.risk_manager.can_trade(opp):
                    # 6. Execute trade
                    result = await self._execute_trade(opp)

                    # 7. Update portfolio
                    self.portfolio.update(result)

                    # 8. Log for analysis
                    self._log_trade(result)

            await asyncio.sleep(0.1)  # 100ms cycle

    def _detect_arbitrage(self, prices):
        opportunities = []

        # Cross-exchange spread
        for pair in self.pairs:
            for ex1, ex2 in itertools.combinations(self.exchanges, 2):
                spread = self._calculate_spread(prices, pair, ex1, ex2)
                if spread > self.min_profit_threshold:
                    opportunities.append(CrossExchangeArb(pair, ex1, ex2, spread))

        # Triangular arbitrage
        for exchange in self.exchanges:
            triangles = self._find_triangular_arb(prices, exchange)
            opportunities.extend(triangles)

        return opportunities
```

### 16.6 Risk Management System

#### Hard Limits (Non-Negotiable)

```python
class RiskManager:
    # HARD LIMITS - Never exceeded
    MAX_DAILY_LOSS = 0.05        # 5% max daily loss
    MAX_WEEKLY_LOSS = 0.15       # 15% max weekly loss
    MAX_DRAWDOWN = 0.25          # 25% max drawdown from peak
    MAX_SINGLE_TRADE_LOSS = 0.02 # 2% max loss per trade
    MAX_POSITION_SIZE = 0.40     # 40% max single position
    MAX_LEVERAGE = 10            # 10x max leverage
    MIN_CASH_RESERVE = 0.10      # 10% always in cash

    def can_trade(self, opportunity):
        # Check all limits
        if self.daily_pnl < -self.MAX_DAILY_LOSS * self.peak_equity:
            return False  # Stop trading for the day

        if self.weekly_pnl < -self.MAX_WEEKLY_LOSS * self.weekly_start:
            return False  # Stop trading for the week

        if self.current_drawdown > self.MAX_DRAWDOWN:
            return False  # In drawdown protection mode

        position_size = self._calculate_position(opportunity)
        if position_size > self.MAX_POSITION_SIZE * self.equity:
            return False

        return True
```

#### Dynamic Risk Adjustment

```
Risk Scaling Based on Performance:

If Weekly Return > +5%:
  → Increase position sizes by 10% (momentum)

If Weekly Return < -3%:
  → Reduce position sizes by 25% (protection)

If Max Drawdown > 15%:
  → Reduce position sizes by 50%
  → Switch to conservative strategies only

If Max Drawdown > 20%:
  → Stop automated trading
  → Require manual review
```

#### Circuit Breakers

| Condition | Action | Duration |
|-----------|--------|----------|
| 3 consecutive losses | Pause 5 minutes | Auto-resume |
| 5% daily loss | Stop for day | Next day |
| 10% weekly loss | Stop for week | Manual reset |
| 20% drawdown | Stop all trading | Manual review |
| Exchange API error | Skip exchange | 1 hour |
| Unusual spread (>5%) | Skip opportunity | 1 minute |

### 16.7 Trade Execution Protocols

#### Pre-Trade Checklist (Automated)

```python
def pre_trade_check(self, opportunity):
    checks = {
        'sufficient_balance': self._check_balance(opportunity),
        'within_risk_limits': self.risk_manager.can_trade(opportunity),
        'spread_still_valid': self._verify_spread(opportunity),
        'exchange_healthy': self._check_exchange_status(opportunity),
        'no_pending_orders': self._check_pending_orders(),
        'within_trading_hours': self._check_trading_hours(opportunity),
    }
    return all(checks.values()), checks
```

#### Order Execution Sequence

**For Cross-Exchange Arbitrage:**
```
1. Verify balances on both exchanges
2. Place SELL order on higher-priced exchange (limit, IOC)
3. If fill confirmed within 100ms:
   → Place BUY order on lower-priced exchange
4. If BUY doesn't fill within 200ms:
   → Cancel and reverse SELL position
5. Record results and update portfolio
```

**For Triangular Arbitrage:**
```
1. Calculate exact quantities for all 3 legs
2. Submit all 3 orders simultaneously
3. Monitor fills:
   - All 3 filled → Success
   - Partial fills → Complete remaining legs at market
   - Failed leg → Unwind positions
4. Maximum execution time: 500ms
5. Cancel all if incomplete after timeout
```

#### Slippage Control

```python
class SlippageManager:
    MAX_SLIPPAGE = 0.002  # 0.2% max slippage

    def calculate_safe_size(self, orderbook, target_amount):
        """Calculate max size that stays within slippage tolerance"""
        cumulative = 0
        total_cost = 0
        mid_price = (orderbook['bids'][0][0] + orderbook['asks'][0][0]) / 2

        for price, size in orderbook['asks']:
            slippage = (price - mid_price) / mid_price
            if slippage > self.MAX_SLIPPAGE:
                break
            cumulative += size
            total_cost += price * size
            if cumulative >= target_amount:
                break

        return min(cumulative, target_amount)
```

### 16.8 Performance Tracking & Reporting

#### Real-Time Dashboard

```
┌──────────────────────────────────────────────────────────────────────┐
│                    ARBITRAGE BOT DASHBOARD                           │
│                    Started: $100.00 | Current: $147.32               │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  PERFORMANCE                          POSITION STATUS                │
│  ─────────────────                    ────────────────               │
│  Today:      +$2.15 (+1.48%)          Open Positions: 2              │
│  This Week:  +$12.45 (+9.2%)          BTC/USDT Long: $25.00          │
│  Total:      +$47.32 (+47.3%)         ETH/BTC Arb: $18.50            │
│  Days Active: 28                                                     │
│  Target Pace: ████████████░░░░ 78%    Cash Reserve: $103.82          │
│                                                                      │
│  RISK METRICS                         TODAY'S TRADES                 │
│  ─────────────                        ──────────────                 │
│  Max Drawdown: 8.2%                   Total: 47                      │
│  Current DD: 2.1%                     Won: 41 (87%)                  │
│  Sharpe (30D): 2.4                    Lost: 6 (13%)                  │
│  Win Rate: 84%                        Avg Win: +0.35%                │
│  Avg Trade: +0.18%                    Avg Loss: -0.42%               │
│                                                                      │
│  STRATEGY BREAKDOWN                                                  │
│  ──────────────────                                                  │
│  Crypto X-Exchange: +$28.50 (42 trades, 88% win)                    │
│  Crypto Triangle:   +$12.20 (156 trades, 82% win)                   │
│  FX Micro:          +$4.80 (18 trades, 78% win)                     │
│  Stablecoin:        +$1.82 (yield, no trades)                       │
│                                                                      │
│  RECENT ACTIVITY                                                     │
│  ───────────────                                                     │
│  14:32:15 | BTC Binance→Coinbase | +$0.42 (+0.31%) | 180ms          │
│  14:31:02 | ETH→BTC→USDT→ETH    | +$0.18 (+0.14%) | 95ms           │
│  14:28:45 | SOL Binance→Kraken  | -$0.15 (-0.12%) | 220ms SLIP     │
│  14:25:33 | EUR/USD stat arb    | +$0.28 (+0.22%) | Closed          │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

#### Daily Report (Automated)

```
DAILY ARBITRAGE REPORT - January 30, 2026
==========================================

ACCOUNT SUMMARY
Starting Balance: $145.17
Ending Balance:   $147.32
Daily P&L:        +$2.15 (+1.48%)
Cumulative P&L:   +$47.32 (+47.3%)

PROGRESS TO GOAL
Days Elapsed:     28 of 60
Target Balance:   $158.74
Actual Balance:   $147.32
Status:           BEHIND PACE (-7.2%)
Required Daily:   1.95% (vs 1.16% target) to catch up

TRADE STATISTICS
Total Trades:     47
Win Rate:         87.2% (41/47)
Profit Factor:    3.8
Average Win:      +$0.52 (+0.35%)
Average Loss:     -$0.62 (-0.42%)
Largest Win:      +$1.85 (BTC cross-exchange)
Largest Loss:     -$0.95 (SOL slippage)

STRATEGY PERFORMANCE
┌────────────────────┬─────────┬────────┬──────────┐
│ Strategy           │ P&L     │ Trades │ Win Rate │
├────────────────────┼─────────┼────────┼──────────┤
│ Crypto X-Exchange  │ +$1.42  │ 12     │ 92%      │
│ Crypto Triangle    │ +$0.58  │ 28     │ 82%      │
│ FX Micro           │ +$0.12  │ 5      │ 80%      │
│ Stablecoin Yield   │ +$0.03  │ -      │ -        │
└────────────────────┴─────────┴────────┴──────────┘

RISK METRICS
Max Intraday Drawdown: 1.2%
Peak Equity Today:     $148.50
Exposure (Avg):        65%
Leverage (Avg):        1.2x

RECOMMENDATIONS
• SOL arbitrage showing high slippage - reduce allocation
• BTC cross-exchange performing well - consider +5% allocation
• FX opportunities limited today - check Asian session
```

### 16.9 Tax Reporting & Compliance System

#### Why This Matters

High-frequency arbitrage trading can generate **hundreds to thousands of trades per month**. Without proper tracking:
- Tax filing becomes nearly impossible
- Audit risk increases significantly
- You may overpay taxes or face penalties
- Cost basis errors compound over time

#### Trade Log Schema (Every Trade Captured)

```python
@dataclass
class TaxableTrade:
    """Complete record for tax reporting - IRS/HMRC compliant"""

    # === IDENTIFICATION ===
    trade_id: str               # Unique ID: "TRD-20260130-143215-001"
    timestamp_utc: datetime     # Exact execution time (UTC)
    timestamp_local: datetime   # Local time for reporting
    tax_year: int               # 2026

    # === ASSET DETAILS ===
    asset_type: str             # "CRYPTO", "FOREX", "COMMODITY", "CFD"
    symbol: str                 # "BTC/USDT", "EUR/USD", "GC"
    asset_name: str             # "Bitcoin", "Euro", "Gold Futures"

    # === TRANSACTION DETAILS ===
    side: str                   # "BUY" or "SELL"
    quantity: Decimal           # Exact amount (use Decimal, not float!)
    price: Decimal              # Execution price
    gross_value: Decimal        # quantity × price
    currency: str               # "USD", "EUR", etc.

    # === COST BASIS (Critical for taxes) ===
    cost_basis_method: str      # "FIFO", "LIFO", "HIFO", "SPECIFIC_ID"
    acquisition_date: datetime  # When asset was originally acquired
    acquisition_price: Decimal  # Original purchase price
    acquisition_cost: Decimal   # Total cost including fees
    holding_period_days: int    # Days held (for short/long-term)

    # === FEES & COSTS ===
    exchange_fee: Decimal       # Trading fee
    network_fee: Decimal        # Blockchain fee (crypto)
    spread_cost: Decimal        # Implicit spread cost
    total_fees: Decimal         # All fees combined

    # === GAIN/LOSS CALCULATION ===
    proceeds: Decimal           # Sale price - fees
    cost_basis: Decimal         # Acquisition cost + fees
    realized_gain_loss: Decimal # proceeds - cost_basis
    gain_loss_type: str         # "SHORT_TERM" or "LONG_TERM"

    # === EXCHANGE/BROKER INFO ===
    exchange: str               # "Binance", "OANDA", etc.
    exchange_trade_id: str      # Exchange's internal ID
    account_id: str             # Account identifier
    order_type: str             # "MARKET", "LIMIT"

    # === ARBITRAGE SPECIFIC ===
    strategy: str               # "CROSS_EXCHANGE", "TRIANGULAR", "STAT_ARB"
    related_trade_ids: List[str] # Linked trades (for multi-leg)
    is_wash_sale: bool          # Wash sale rule flag
    wash_sale_adjustment: Decimal # Disallowed loss amount

    # === AUDIT TRAIL ===
    raw_exchange_response: str  # JSON of exchange API response
    order_id: str               # Original order ID
    fill_id: str                # Fill/execution ID
    notes: str                  # Any manual notes
```

#### Database Storage Structure

```sql
-- Primary trade log table
CREATE TABLE trade_log (
    trade_id VARCHAR(50) PRIMARY KEY,
    timestamp_utc TIMESTAMP NOT NULL,
    tax_year INT NOT NULL,

    -- Asset info
    asset_type VARCHAR(20) NOT NULL,
    symbol VARCHAR(20) NOT NULL,
    side VARCHAR(4) NOT NULL,

    -- Amounts (stored as integers in smallest unit to avoid float errors)
    quantity_raw BIGINT NOT NULL,
    quantity_decimals INT NOT NULL,
    price_raw BIGINT NOT NULL,
    price_decimals INT NOT NULL,

    -- Cost basis
    cost_basis_method VARCHAR(20) NOT NULL,
    acquisition_date TIMESTAMP,
    acquisition_price_raw BIGINT,
    holding_period_days INT,

    -- Fees
    exchange_fee_raw BIGINT DEFAULT 0,
    network_fee_raw BIGINT DEFAULT 0,
    total_fees_raw BIGINT DEFAULT 0,

    -- Gain/Loss
    proceeds_raw BIGINT,
    cost_basis_raw BIGINT,
    realized_gain_loss_raw BIGINT,
    gain_loss_type VARCHAR(15),

    -- Metadata
    exchange VARCHAR(50) NOT NULL,
    exchange_trade_id VARCHAR(100),
    strategy VARCHAR(50),
    is_wash_sale BOOLEAN DEFAULT FALSE,
    wash_sale_adjustment_raw BIGINT DEFAULT 0,

    -- Audit
    raw_response JSONB,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,

    -- Indexes for tax reporting queries
    INDEX idx_tax_year (tax_year),
    INDEX idx_timestamp (timestamp_utc),
    INDEX idx_asset (asset_type, symbol),
    INDEX idx_gain_loss_type (gain_loss_type)
);

-- Lot tracking for cost basis (FIFO/LIFO/HIFO)
CREATE TABLE asset_lots (
    lot_id VARCHAR(50) PRIMARY KEY,
    asset_symbol VARCHAR(20) NOT NULL,
    acquisition_date TIMESTAMP NOT NULL,
    acquisition_price_raw BIGINT NOT NULL,
    original_quantity_raw BIGINT NOT NULL,
    remaining_quantity_raw BIGINT NOT NULL,
    exchange VARCHAR(50) NOT NULL,
    source_trade_id VARCHAR(50),
    is_depleted BOOLEAN DEFAULT FALSE,

    INDEX idx_asset_fifo (asset_symbol, acquisition_date),
    INDEX idx_remaining (asset_symbol, is_depleted)
);

-- Daily P&L summary for quick reporting
CREATE TABLE daily_summary (
    date DATE PRIMARY KEY,
    tax_year INT NOT NULL,
    total_trades INT,
    gross_proceeds_raw BIGINT,
    total_cost_basis_raw BIGINT,
    total_fees_raw BIGINT,
    net_short_term_gain_raw BIGINT,
    net_long_term_gain_raw BIGINT,
    wash_sale_adjustments_raw BIGINT
);
```

#### Cost Basis Methods Supported

| Method | Description | Best For | IRS Compliant |
|--------|-------------|----------|---------------|
| **FIFO** | First In, First Out | Default, simple | Yes |
| **LIFO** | Last In, First Out | Tax-loss harvesting | Yes |
| **HIFO** | Highest In, First Out | Minimize gains | Yes |
| **Specific ID** | Choose exact lot | Maximum control | Yes (if documented) |

```python
class CostBasisTracker:
    def __init__(self, method="FIFO"):
        self.method = method
        self.lots = defaultdict(list)  # asset -> list of lots

    def add_lot(self, asset, quantity, price, date, trade_id):
        """Record new acquisition"""
        lot = {
            'lot_id': f"LOT-{trade_id}",
            'quantity': Decimal(str(quantity)),
            'remaining': Decimal(str(quantity)),
            'price': Decimal(str(price)),
            'date': date,
            'trade_id': trade_id
        }
        self.lots[asset].append(lot)

    def consume_lots(self, asset, quantity, sale_date):
        """Consume lots based on method, return cost basis info"""
        quantity = Decimal(str(quantity))
        consumed = []
        remaining = quantity

        # Sort lots based on method
        if self.method == "FIFO":
            sorted_lots = sorted(self.lots[asset], key=lambda x: x['date'])
        elif self.method == "LIFO":
            sorted_lots = sorted(self.lots[asset], key=lambda x: x['date'], reverse=True)
        elif self.method == "HIFO":
            sorted_lots = sorted(self.lots[asset], key=lambda x: x['price'], reverse=True)

        for lot in sorted_lots:
            if remaining <= 0:
                break
            if lot['remaining'] <= 0:
                continue

            take = min(remaining, lot['remaining'])
            lot['remaining'] -= take
            remaining -= take

            holding_days = (sale_date - lot['date']).days
            consumed.append({
                'lot_id': lot['lot_id'],
                'quantity': take,
                'cost_basis': take * lot['price'],
                'acquisition_date': lot['date'],
                'holding_period_days': holding_days,
                'is_long_term': holding_days > 365
            })

        return consumed
```

#### Wash Sale Detection (US Tax Rule)

```python
class WashSaleDetector:
    """
    IRS Wash Sale Rule: Cannot claim loss if you buy "substantially
    identical" security within 30 days before or after the sale.
    """
    WASH_SALE_WINDOW = 30  # days

    def check_wash_sale(self, sale_trade, all_trades):
        if sale_trade.realized_gain_loss >= 0:
            return False, Decimal('0')  # Only applies to losses

        # Look for purchases 30 days before/after
        window_start = sale_trade.timestamp - timedelta(days=self.WASH_SALE_WINDOW)
        window_end = sale_trade.timestamp + timedelta(days=self.WASH_SALE_WINDOW)

        repurchases = [
            t for t in all_trades
            if t.symbol == sale_trade.symbol
            and t.side == "BUY"
            and window_start <= t.timestamp <= window_end
            and t.trade_id != sale_trade.trade_id
        ]

        if repurchases:
            # Loss is disallowed, but added to cost basis of repurchase
            disallowed_loss = abs(sale_trade.realized_gain_loss)
            return True, disallowed_loss

        return False, Decimal('0')
```

#### Tax Report Generation

**US Form 8949 Format (Crypto & Securities)**
```
┌────────────────────────────────────────────────────────────────────────────┐
│ FORM 8949 - Sales and Other Dispositions of Capital Assets                │
│ Tax Year: 2026                                                             │
├────────────────────────────────────────────────────────────────────────────┤
│ Part I: Short-Term (held 1 year or less)                                   │
├──────────────┬──────────┬──────────┬──────────┬──────────┬────────────────┤
│ Description  │ Acquired │ Sold     │ Proceeds │ Cost     │ Gain/(Loss)    │
├──────────────┼──────────┼──────────┼──────────┼──────────┼────────────────┤
│ 0.5 BTC      │ 01/15/26 │ 01/20/26 │ $21,500  │ $21,200  │ $300           │
│ 2.0 ETH      │ 01/18/26 │ 01/22/26 │ $4,850   │ $4,920   │ ($70) W        │
│ 100 EUR/USD  │ 01/25/26 │ 01/25/26 │ $108.50  │ $108.00  │ $0.50          │
│ ...          │          │          │          │          │                │
├──────────────┴──────────┴──────────┴──────────┴──────────┴────────────────┤
│ TOTALS: 1,247 transactions                                                 │
│ Total Proceeds: $847,250    Total Cost: $839,180    Net Gain: $8,070      │
│ Wash Sale Adjustments: $2,450                                              │
└────────────────────────────────────────────────────────────────────────────┘
```

**Automated Report Generator:**
```python
class TaxReportGenerator:
    def generate_form_8949(self, tax_year):
        """Generate IRS Form 8949 compatible report"""
        trades = self.db.get_trades_by_year(tax_year)

        short_term = [t for t in trades if t.holding_period_days <= 365]
        long_term = [t for t in trades if t.holding_period_days > 365]

        report = {
            'tax_year': tax_year,
            'generated_at': datetime.utcnow().isoformat(),

            'short_term': {
                'transactions': len(short_term),
                'total_proceeds': sum(t.proceeds for t in short_term),
                'total_cost_basis': sum(t.cost_basis for t in short_term),
                'total_gain_loss': sum(t.realized_gain_loss for t in short_term),
                'wash_sale_adjustments': sum(t.wash_sale_adjustment for t in short_term),
                'trades': [self._format_8949_row(t) for t in short_term]
            },

            'long_term': {
                'transactions': len(long_term),
                'total_proceeds': sum(t.proceeds for t in long_term),
                'total_cost_basis': sum(t.cost_basis for t in long_term),
                'total_gain_loss': sum(t.realized_gain_loss for t in long_term),
                'trades': [self._format_8949_row(t) for t in long_term]
            },

            'summary': {
                'total_transactions': len(trades),
                'net_short_term': sum(t.realized_gain_loss for t in short_term),
                'net_long_term': sum(t.realized_gain_loss for t in long_term),
                'total_fees_paid': sum(t.total_fees for t in trades)
            }
        }

        return report

    def export_csv(self, tax_year, format='turbo_tax'):
        """Export in format compatible with tax software"""
        trades = self.db.get_trades_by_year(tax_year)

        if format == 'turbo_tax':
            headers = ['Currency Name', 'Purchase Date', 'Cost Basis',
                      'Date Sold', 'Proceeds', 'Gain/Loss']
        elif format == 'tax_act':
            headers = ['Description', 'Date Acquired', 'Date Sold',
                      'Proceeds', 'Cost Basis', 'Gain/Loss', 'Term']
        elif format == 'crypto_tax_calculator':
            headers = ['Timestamp', 'Type', 'Asset', 'Amount', 'Price',
                      'Fee', 'Exchange', 'Cost Basis', 'Proceeds', 'Gain']

        rows = [self._format_row(t, format) for t in trades]
        return self._to_csv(headers, rows)
```

#### Crypto-Specific Considerations

| Event | Tax Treatment (US) | Tracking Required |
|-------|-------------------|-------------------|
| Buy crypto with USD | Not taxable | Record cost basis |
| Sell crypto for USD | Taxable gain/loss | Calculate from cost basis |
| Crypto-to-crypto trade | **Taxable event** | Both sides recorded |
| Receive staking rewards | **Ordinary income** | FMV at receipt |
| DeFi yield | **Ordinary income** | FMV at receipt |
| Transfer between wallets | Not taxable | Track for cost basis |
| Gas/network fees | Add to cost basis | Record all fees |

**Crypto-to-Crypto Handling:**
```python
def record_crypto_swap(self, from_asset, to_asset, from_amount, to_amount, timestamp):
    """
    BTC → ETH swap is TWO taxable events:
    1. Sell BTC (realize gain/loss)
    2. Buy ETH (establish new cost basis)
    """
    # Step 1: Calculate BTC sale
    btc_fmv = self.get_fair_market_value('BTC', timestamp)
    btc_proceeds = from_amount * btc_fmv

    btc_sale = self.record_sale(
        asset='BTC',
        quantity=from_amount,
        proceeds=btc_proceeds,
        timestamp=timestamp
    )

    # Step 2: Record ETH purchase at same value
    eth_cost_basis = btc_proceeds  # What you "paid" in USD terms

    self.cost_basis_tracker.add_lot(
        asset='ETH',
        quantity=to_amount,
        price=eth_cost_basis / to_amount,
        date=timestamp,
        trade_id=f"{btc_sale.trade_id}-swap"
    )

    return btc_sale
```

#### Forex (Section 988 vs Section 1256)

| Treatment | Section 988 | Section 1256 |
|-----------|-------------|--------------|
| Default for | Spot forex | Futures, options |
| Tax rate | Ordinary income | 60% long-term, 40% short-term |
| Loss limit | Unlimited | $3,000/year |
| Mark-to-market | No | Yes (year-end) |
| Election | Can opt out | Default for contracts |

```python
def categorize_forex_trade(self, trade):
    """Determine tax treatment for forex"""
    if trade.instrument_type in ['FUTURE', 'OPTION']:
        return 'SECTION_1256'  # 60/40 treatment
    elif trade.instrument_type == 'SPOT':
        if self.has_1256_election:
            return 'SECTION_1256'
        return 'SECTION_988'  # Ordinary income/loss
```

#### Monthly Tax Estimate Report

```
┌────────────────────────────────────────────────────────────────────────────┐
│              MONTHLY TAX ESTIMATE - January 2026                           │
├────────────────────────────────────────────────────────────────────────────┤
│                                                                            │
│  TRADING ACTIVITY                                                          │
│  ─────────────────                                                         │
│  Total Trades:              1,847                                          │
│  Crypto Trades:             1,523 (all short-term)                         │
│  Forex Trades:              312 (Section 988)                              │
│  CFD Trades:                12                                             │
│                                                                            │
│  REALIZED GAINS/LOSSES                                                     │
│  ─────────────────────                                                     │
│  Crypto Short-Term Gains:   $892.45                                        │
│  Crypto Short-Term Losses:  ($156.20)                                      │
│  Net Crypto:                $736.25                                        │
│                                                                            │
│  Forex (Section 988):       $124.80 (ordinary income)                      │
│  CFD Gains:                 $18.50                                         │
│                                                                            │
│  TOTAL TAXABLE:             $879.55                                        │
│                                                                            │
│  ESTIMATED TAX LIABILITY                                                   │
│  ────────────────────────                                                  │
│  Assuming 32% bracket (short-term + ordinary):                             │
│  Federal:                   $281.46                                        │
│  State (CA 9.3%):           $81.80                                         │
│  Total Estimated:           $363.26                                        │
│                                                                            │
│  QUARTERLY ESTIMATE (if annualized):                                       │
│  Q1 Estimated Payment:      $1,089.78 (due April 15)                       │
│                                                                            │
│  WASH SALES THIS MONTH:     3 trades, $45.20 disallowed                   │
│                                                                            │
│  COST BASIS INVENTORY                                                      │
│  ────────────────────                                                      │
│  BTC lots held: 12 (oldest: 01/05/26, newest: 01/30/26)                   │
│  ETH lots held: 8 (oldest: 01/08/26, newest: 01/29/26)                    │
│  USD stablecoin: $45.20 (no tax impact)                                   │
│                                                                            │
└────────────────────────────────────────────────────────────────────────────┘
```

#### Integration with Tax Software

| Software | Export Format | Automation |
|----------|--------------|------------|
| **TurboTax** | CSV, TXF | Direct import |
| **H&R Block** | CSV | Manual upload |
| **TaxAct** | CSV | Direct import |
| **CoinTracker** | API sync | Real-time |
| **Koinly** | API sync | Real-time |
| **TokenTax** | CSV, API | Both supported |
| **ZenLedger** | API sync | Real-time |

**Auto-sync with Crypto Tax Services:**
```python
class TaxServiceSync:
    def sync_to_koinly(self, api_key):
        """Push trades to Koinly for automatic tax calculation"""
        trades = self.get_unsynced_trades()

        for trade in trades:
            koinly_format = {
                'date': trade.timestamp.isoformat(),
                'type': 'sell' if trade.side == 'SELL' else 'buy',
                'from_amount': str(trade.quantity) if trade.side == 'SELL' else None,
                'from_currency': trade.symbol.split('/')[0] if trade.side == 'SELL' else None,
                'to_amount': str(trade.quantity) if trade.side == 'BUY' else None,
                'to_currency': trade.symbol.split('/')[0] if trade.side == 'BUY' else None,
                'fee_amount': str(trade.total_fees),
                'fee_currency': 'USD',
                'exchange': trade.exchange,
                'external_id': trade.trade_id
            }
            self.koinly_api.create_transaction(koinly_format)
            trade.mark_synced('koinly')
```

#### Audit Trail & Record Retention

**IRS requires 3-7 years of records. We keep everything.**

```python
class AuditTrailManager:
    def log_trade_complete(self, trade, raw_response):
        """Store complete audit trail for every trade"""

        audit_record = {
            'trade_id': trade.trade_id,
            'timestamp': datetime.utcnow(),

            # Original exchange response (proof)
            'exchange_response': raw_response,

            # Screenshots/state at time of trade
            'orderbook_snapshot': self.capture_orderbook(trade.symbol),
            'balance_before': self.get_balance_snapshot(),
            'balance_after': None,  # Filled after confirmation

            # Calculation audit
            'cost_basis_calculation': {
                'method': trade.cost_basis_method,
                'lots_consumed': trade.consumed_lots,
                'remaining_lots': self.get_remaining_lots(trade.symbol)
            },

            # System state
            'system_version': self.version,
            'config_hash': self.get_config_hash()
        }

        # Store in append-only audit log
        self.audit_db.insert(audit_record)

        # Also backup to immutable storage
        self.backup_to_s3(audit_record)
```

**Record Retention Policy:**
```
Trade Records:        Keep forever (cost basis needed for future sales)
Daily Summaries:      Keep 10 years
Exchange Statements:  Keep 7 years
Tax Reports:          Keep 7 years
Audit Logs:           Keep forever
API Responses:        Keep 3 years (can compress after)
```

### 16.10 Scaling Plan

As the account grows, unlock additional strategies:

```
$100 → $200 (Days 1-60)
├── Primary: Crypto spot arbitrage
├── Secondary: Crypto triangular
├── Goal: Prove system works
└── Reinvest: 100% of profits

$200 → $500 (Days 61-90)
├── Add: More exchange pairs
├── Add: Larger position sizes
├── Add: Micro FX with 20:1 leverage
└── Reinvest: 90% of profits

$500 → $2000 (Days 91-150)
├── Add: Commodity CFDs
├── Add: Crypto futures (basis trade)
├── Add: Multiple simultaneous strategies
└── Reinvest: 80% of profits

$2000 → $10000 (Days 151-240)
├── Add: Micro futures (ES, NQ, GC)
├── Add: Options strategies
├── Add: More sophisticated stat arb
└── Reinvest: 70% of profits

$10000+ (Day 241+)
├── Full strategy suite available
├── Consider professional infrastructure
├── Tax optimization strategies
└── Reinvest: 50%, withdraw 50%
```

### 16.11 Emergency Procedures

#### Automatic Shutdown Conditions

```python
EMERGENCY_SHUTDOWN_CONDITIONS = [
    ('daily_loss', lambda x: x < -0.10),      # 10% daily loss
    ('drawdown', lambda x: x > 0.30),          # 30% drawdown
    ('exchange_error_rate', lambda x: x > 0.5), # 50% API errors
    ('balance_discrepancy', lambda x: x > 0.05), # 5% balance mismatch
    ('unusual_volatility', lambda x: x > 5.0),  # 5x normal vol
]

def check_emergency_conditions(self):
    for name, condition in EMERGENCY_SHUTDOWN_CONDITIONS:
        value = getattr(self.metrics, name)
        if condition(value):
            self._emergency_shutdown(reason=name)
            self._alert_operator(f"EMERGENCY: {name} triggered")
            return True
    return False
```

#### Manual Override Commands

```
/stop              - Stop all trading immediately
/pause             - Pause new trades, keep positions
/close_all         - Close all positions at market
/status            - Get full system status
/risk reduce 50    - Reduce all position sizes by 50%
/withdraw <amount> - Initiate withdrawal
/resume            - Resume trading after pause
```

### 16.12 Legal & Compliance Notes

**Disclaimer**: This system is for educational and research purposes. Before trading with real money:

1. **Verify legality** in your jurisdiction
2. **Understand tax implications** of frequent trading
3. **Accept that losses are possible** despite arbitrage being "low risk"
4. **Start with paper trading** to validate the system
5. **Never trade money you can't afford to lose**

**Crypto-specific**:
- Verify exchange is licensed in your jurisdiction
- Understand withdrawal limits and KYC requirements
- Be aware of potential exchange insolvency risk

**Forex-specific**:
- Use regulated brokers (NFA in US, FCA in UK)
- Understand leverage risks
- Be aware of swap/rollover costs

---

## 17. Glossary

| Term | Definition |
|------|------------|
| **Basis** | Price difference between related instruments (spot vs futures, or same asset in different markets) |
| **Carry** | Interest rate differential between two currencies |
| **Contango** | Futures price > spot price (typical for commodities with storage costs) |
| **Backwardation** | Spot price > futures price (supply shortage signal) |
| **NDF** | Non-Deliverable Forward - settled in USD for restricted currencies |
| **Crack Spread** | Refining margin (product prices minus crude) |
| **Spark Spread** | Power generation margin (electricity minus fuel cost) |
| **Z-Score** | Standard deviations from mean |
| **Half-Life** | Time for mean-reverting series to revert 50% |
| **Cointegration** | Long-term equilibrium relationship between series |
| **Sharpe Ratio** | Risk-adjusted return (return / volatility) |

---

*Document Version: 3.1*
*Last Updated: January 2026*
*Author: Arbitrage Analysis Team*

**Version History:**
- v1.0: Initial plan with G10 currencies and precious metals
- v2.0: Added 30+ EM currencies, energy, agricultural commodities, strategic metals, free data sources
- v3.0: Added complete trading execution module for $100 account targeting 2x in 60 days
- v3.1: Added comprehensive tax reporting system with IRS-compliant trade logging, cost basis tracking, wash sale detection, and tax software integration
