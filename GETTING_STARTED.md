# Getting Started: Arbitrage Trading System

This guide walks you through setting up and launching the arbitrage trading system from zero to live trading.

---

## Prerequisites

- $100 starting capital
- Computer with Python 3.9+
- Stable internet connection
- Government ID for exchange verification (KYC)

---

## Phase 1: Account Setup (Day 1-3)

### Step 1: Create Exchange Accounts

You'll need accounts on multiple exchanges to execute cross-exchange arbitrage.

| Exchange | URL | Purpose | KYC Time |
|----------|-----|---------|----------|
| Binance | https://binance.com | Primary crypto trading | 1-3 days |
| Coinbase Pro | https://pro.coinbase.com | US-regulated, fiat on-ramp | 1-3 days |
| Kraken | https://kraken.com | EUR pairs, backup exchange | 1-3 days |
| OANDA | https://oanda.com | Forex micro-lot trading | Same day |

**Action Items:**
```
[ ] Sign up for Binance account
[ ] Complete Binance KYC verification (photo ID + selfie)
[ ] Sign up for Coinbase Pro account
[ ] Complete Coinbase KYC verification
[ ] Sign up for Kraken account (optional but recommended)
[ ] Sign up for OANDA account
[ ] Wait for all verifications to complete
```

### Step 2: Enable API Access

Each exchange requires API keys for programmatic trading.

#### Binance API Setup
1. Log in to Binance
2. Go to **Settings → API Management**
3. Click **Create API**
4. Label it "ArbitrageBot"
5. Complete 2FA verification
6. Enable permissions:
   - [x] Read Info
   - [x] Enable Spot & Margin Trading
   - [ ] Enable Withdrawals (leave OFF for security)
7. Restrict to your IP address (recommended)
8. Save your **API Key** and **Secret Key** securely

#### Coinbase Pro API Setup
1. Log in to Coinbase Pro
2. Go to **Profile → API**
3. Click **+ New API Key**
4. Select portfolio: Default
5. Set permissions:
   - [x] View
   - [x] Trade
   - [ ] Transfer (leave OFF)
6. Create passphrase (save it!)
7. Save your **API Key**, **Secret**, and **Passphrase**

#### Kraken API Setup
1. Log in to Kraken
2. Go to **Settings → API**
3. Click **Generate New Key**
4. Set permissions:
   - [x] Query Funds
   - [x] Query Open Orders & Trades
   - [x] Create & Modify Orders
5. Save your **API Key** and **Private Key**

#### OANDA API Setup
1. Log in to OANDA
2. Go to **Manage API Access**
3. Click **Generate** under Personal Access Token
4. Note your **Account ID** (shown in account details)
5. Save your **Access Token**

### Step 3: Fund Your Accounts

Distribute your $100 according to the strategy allocation:

| Account | Amount | Purpose |
|---------|--------|---------|
| Binance | $40 | Cross-exchange arbitrage |
| Coinbase Pro | $25 | Triangular arbitrage |
| OANDA | $20 | Forex micro-lot trading |
| Binance (stablecoins) | $15 | Yield + stablecoin arb |

**Funding Methods:**
- Bank transfer (ACH): Free, 3-5 days
- Wire transfer: $10-30 fee, 1-2 days
- Debit card: 2-4% fee, instant
- Crypto transfer: Network fees, minutes

**Action Items:**
```
[ ] Deposit $65 to Binance ($40 trading + $25 stablecoins → will transfer $25 to Coinbase)
    OR deposit directly to each exchange
[ ] Deposit $20 to OANDA
[ ] Convert $15 to USDT/USDC on Binance for stablecoin allocation
[ ] Verify all balances are available for trading
```

---

## Phase 2: Development Environment (Day 1-2)

### Step 4: Install Required Software

#### Install Python
```bash
# Check if Python is installed
python3 --version  # Should be 3.9 or higher

# If not installed:
# macOS: brew install python3
# Ubuntu: sudo apt install python3 python3-pip python3-venv
# Windows: Download from python.org
```

#### Create Project Directory
```bash
mkdir arbitrage-bot
cd arbitrage-bot
```

#### Set Up Virtual Environment
```bash
# Create virtual environment
python3 -m venv venv

# Activate it
source venv/bin/activate        # macOS/Linux
# OR
venv\Scripts\activate           # Windows

# Verify activation (should show venv path)
which python
```

#### Install Dependencies
```bash
# Core trading libraries
pip install ccxt                 # Unified exchange API (supports 100+ exchanges)
pip install oandapyV20           # OANDA forex API

# Data processing
pip install pandas numpy         # Data manipulation
pip install yfinance             # Free market data backup

# Database
pip install sqlalchemy           # Database ORM
pip install alembic              # Database migrations

# Async operations
pip install aiohttp              # Async HTTP client
pip install websockets           # WebSocket connections
pip install asyncio              # Async framework

# Utilities
pip install python-dotenv        # Environment variable management
pip install python-dateutil      # Date parsing
pip install requests             # HTTP requests

# Optional but recommended
pip install rich                 # Beautiful terminal output
pip install schedule             # Task scheduling
```

#### Save Dependencies
```bash
pip freeze > requirements.txt
```

### Step 5: Create Configuration File

**SECURITY WARNING**: Never commit API keys to git!

#### Create .env file
```bash
touch .env
echo ".env" >> .gitignore
```

#### Add your credentials to .env
```env
# Binance
BINANCE_API_KEY=your_binance_api_key_here
BINANCE_SECRET=your_binance_secret_here

# Coinbase Pro
COINBASE_API_KEY=your_coinbase_api_key_here
COINBASE_SECRET=your_coinbase_secret_here
COINBASE_PASSPHRASE=your_coinbase_passphrase_here

# Kraken (optional)
KRAKEN_API_KEY=your_kraken_api_key_here
KRAKEN_SECRET=your_kraken_secret_here

# OANDA
OANDA_ACCOUNT_ID=your_account_id_here
OANDA_ACCESS_TOKEN=your_access_token_here
OANDA_ENVIRONMENT=practice  # Change to 'live' for real trading

# Application Settings
LOG_LEVEL=INFO
DATABASE_URL=sqlite:///arbitrage.db
MIN_PROFIT_THRESHOLD=0.001  # 0.1% minimum profit
MAX_POSITION_SIZE=0.40      # 40% of capital max
```

#### Create config loader (config.py)
```python
import os
from dotenv import load_dotenv

load_dotenv()

class Config:
    # Exchange credentials
    BINANCE_API_KEY = os.getenv('BINANCE_API_KEY')
    BINANCE_SECRET = os.getenv('BINANCE_SECRET')

    COINBASE_API_KEY = os.getenv('COINBASE_API_KEY')
    COINBASE_SECRET = os.getenv('COINBASE_SECRET')
    COINBASE_PASSPHRASE = os.getenv('COINBASE_PASSPHRASE')

    OANDA_ACCOUNT_ID = os.getenv('OANDA_ACCOUNT_ID')
    OANDA_ACCESS_TOKEN = os.getenv('OANDA_ACCESS_TOKEN')

    # Trading parameters
    MIN_PROFIT_THRESHOLD = float(os.getenv('MIN_PROFIT_THRESHOLD', 0.001))
    MAX_POSITION_SIZE = float(os.getenv('MAX_POSITION_SIZE', 0.40))

    # Database
    DATABASE_URL = os.getenv('DATABASE_URL', 'sqlite:///arbitrage.db')
```

### Step 6: Set Up Database

The system uses SQLite by default (no installation needed).

#### Create database schema (models.py)
```python
from sqlalchemy import create_engine, Column, Integer, String, Float, DateTime, Boolean
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker
from datetime import datetime

Base = declarative_base()

class Trade(Base):
    __tablename__ = 'trades'

    id = Column(Integer, primary_key=True)
    trade_id = Column(String(50), unique=True)
    timestamp = Column(DateTime, default=datetime.utcnow)

    # Asset details
    symbol = Column(String(20))
    side = Column(String(4))  # BUY/SELL
    quantity = Column(Float)
    price = Column(Float)

    # Cost basis
    cost_basis = Column(Float)
    realized_pnl = Column(Float)

    # Fees
    exchange_fee = Column(Float)

    # Metadata
    exchange = Column(String(50))
    strategy = Column(String(50))

class DailySummary(Base):
    __tablename__ = 'daily_summary'

    id = Column(Integer, primary_key=True)
    date = Column(DateTime)
    total_trades = Column(Integer)
    total_pnl = Column(Float)
    win_rate = Column(Float)

# Initialize database
engine = create_engine('sqlite:///arbitrage.db')
Base.metadata.create_all(engine)
Session = sessionmaker(bind=engine)
```

**Action Items:**
```
[ ] Install Python 3.9+
[ ] Create project directory
[ ] Set up virtual environment
[ ] Install all dependencies
[ ] Create .env file with API credentials
[ ] Create config.py
[ ] Create models.py and initialize database
[ ] Test imports: python -c "import ccxt; print('OK')"
```

---

## Phase 3: Build Core Components (Day 2-5)

### Step 7: Implement Exchange Adapters

Create a unified interface to interact with all exchanges.

#### Create exchanges.py
```python
import ccxt
import oandapyV20
from oandapyV20.endpoints import pricing, orders
from config import Config

class ExchangeManager:
    def __init__(self):
        self.exchanges = {}
        self._init_binance()
        self._init_coinbase()
        self._init_oanda()

    def _init_binance(self):
        self.exchanges['binance'] = ccxt.binance({
            'apiKey': Config.BINANCE_API_KEY,
            'secret': Config.BINANCE_SECRET,
            'enableRateLimit': True,
        })

    def _init_coinbase(self):
        self.exchanges['coinbase'] = ccxt.coinbasepro({
            'apiKey': Config.COINBASE_API_KEY,
            'secret': Config.COINBASE_SECRET,
            'password': Config.COINBASE_PASSPHRASE,
            'enableRateLimit': True,
        })

    def _init_oanda(self):
        self.oanda = oandapyV20.API(
            access_token=Config.OANDA_ACCESS_TOKEN,
            environment="practice"  # Change to "live" for real
        )
        self.oanda_account = Config.OANDA_ACCOUNT_ID

    def get_price(self, exchange, symbol):
        """Get current price from exchange"""
        ticker = self.exchanges[exchange].fetch_ticker(symbol)
        return {
            'bid': ticker['bid'],
            'ask': ticker['ask'],
            'mid': (ticker['bid'] + ticker['ask']) / 2
        }

    def get_balance(self, exchange):
        """Get account balance"""
        if exchange == 'oanda':
            # OANDA balance logic
            pass
        return self.exchanges[exchange].fetch_balance()

    def place_order(self, exchange, symbol, side, amount, price=None):
        """Place order on exchange"""
        ex = self.exchanges[exchange]
        if price:
            return ex.create_limit_order(symbol, side, amount, price)
        return ex.create_market_order(symbol, side, amount)
```

#### Test connectivity
```python
# test_exchanges.py
from exchanges import ExchangeManager

em = ExchangeManager()

# Test Binance
print("Binance BTC price:", em.get_price('binance', 'BTC/USDT'))
print("Binance balance:", em.get_balance('binance'))

# Test Coinbase
print("Coinbase BTC price:", em.get_price('coinbase', 'BTC/USD'))
```

### Step 8: Implement Arbitrage Detection

#### Create arbitrage.py
```python
from exchanges import ExchangeManager
from itertools import combinations

class ArbitrageDetector:
    def __init__(self, min_profit=0.001):
        self.em = ExchangeManager()
        self.min_profit = min_profit  # 0.1% minimum

    def find_cross_exchange_arb(self, symbol='BTC/USDT'):
        """Find price differences across exchanges"""
        prices = {}

        for exchange in ['binance', 'coinbase']:
            try:
                prices[exchange] = self.em.get_price(exchange, symbol)
            except Exception as e:
                print(f"Error fetching {exchange}: {e}")
                continue

        opportunities = []

        for ex1, ex2 in combinations(prices.keys(), 2):
            # Buy on ex1, sell on ex2
            buy_price = prices[ex1]['ask']
            sell_price = prices[ex2]['bid']
            spread = (sell_price - buy_price) / buy_price

            if spread > self.min_profit:
                opportunities.append({
                    'buy_exchange': ex1,
                    'sell_exchange': ex2,
                    'buy_price': buy_price,
                    'sell_price': sell_price,
                    'spread': spread,
                    'symbol': symbol
                })

            # Check reverse direction
            buy_price = prices[ex2]['ask']
            sell_price = prices[ex1]['bid']
            spread = (sell_price - buy_price) / buy_price

            if spread > self.min_profit:
                opportunities.append({
                    'buy_exchange': ex2,
                    'sell_exchange': ex1,
                    'buy_price': buy_price,
                    'sell_price': sell_price,
                    'spread': spread,
                    'symbol': symbol
                })

        return opportunities

    def find_triangular_arb(self, exchange='binance'):
        """Find triangular arbitrage within single exchange"""
        # Example: BTC -> ETH -> USDT -> BTC
        try:
            btc_usdt = self.em.get_price(exchange, 'BTC/USDT')
            eth_usdt = self.em.get_price(exchange, 'ETH/USDT')
            eth_btc = self.em.get_price(exchange, 'ETH/BTC')

            # Path 1: USDT -> BTC -> ETH -> USDT
            start = 100  # $100
            btc = start / btc_usdt['ask']
            eth = btc / eth_btc['ask']
            end = eth * eth_usdt['bid']
            profit1 = (end - start) / start

            # Path 2: USDT -> ETH -> BTC -> USDT
            eth = start / eth_usdt['ask']
            btc = eth * eth_btc['bid']
            end = btc * btc_usdt['bid']
            profit2 = (end - start) / start

            opportunities = []
            if profit1 > self.min_profit:
                opportunities.append({
                    'path': 'USDT->BTC->ETH->USDT',
                    'profit': profit1,
                    'exchange': exchange
                })
            if profit2 > self.min_profit:
                opportunities.append({
                    'path': 'USDT->ETH->BTC->USDT',
                    'profit': profit2,
                    'exchange': exchange
                })

            return opportunities

        except Exception as e:
            print(f"Error in triangular arb: {e}")
            return []
```

### Step 9: Implement Risk Manager

#### Create risk.py
```python
from datetime import datetime, timedelta

class RiskManager:
    # Hard limits
    MAX_DAILY_LOSS = 0.05        # 5%
    MAX_WEEKLY_LOSS = 0.15       # 15%
    MAX_POSITION_SIZE = 0.40    # 40%
    MAX_DRAWDOWN = 0.25         # 25%

    def __init__(self, starting_capital=100):
        self.starting_capital = starting_capital
        self.peak_equity = starting_capital
        self.daily_pnl = 0
        self.weekly_pnl = 0
        self.trades_today = []

    def can_trade(self, position_size, current_equity):
        """Check if trade is allowed within risk limits"""

        # Check daily loss limit
        if self.daily_pnl < -self.MAX_DAILY_LOSS * self.starting_capital:
            return False, "Daily loss limit reached"

        # Check weekly loss limit
        if self.weekly_pnl < -self.MAX_WEEKLY_LOSS * self.starting_capital:
            return False, "Weekly loss limit reached"

        # Check position size
        if position_size > self.MAX_POSITION_SIZE * current_equity:
            return False, "Position too large"

        # Check drawdown
        drawdown = (self.peak_equity - current_equity) / self.peak_equity
        if drawdown > self.MAX_DRAWDOWN:
            return False, "Max drawdown exceeded"

        return True, "OK"

    def record_trade(self, pnl):
        """Record trade result"""
        self.daily_pnl += pnl
        self.weekly_pnl += pnl
        self.trades_today.append({
            'time': datetime.utcnow(),
            'pnl': pnl
        })

    def reset_daily(self):
        """Reset daily counters"""
        self.daily_pnl = 0
        self.trades_today = []

    def update_peak(self, current_equity):
        """Update peak equity for drawdown calculation"""
        if current_equity > self.peak_equity:
            self.peak_equity = current_equity
```

### Step 10: Implement Trade Logger

#### Create logger.py
```python
from models import Trade, Session
from datetime import datetime
from decimal import Decimal
import uuid

class TradeLogger:
    def __init__(self):
        self.session = Session()

    def log_trade(self, trade_data):
        """Log trade to database for tax reporting"""
        trade = Trade(
            trade_id=f"TRD-{datetime.utcnow().strftime('%Y%m%d-%H%M%S')}-{uuid.uuid4().hex[:4]}",
            timestamp=datetime.utcnow(),
            symbol=trade_data['symbol'],
            side=trade_data['side'],
            quantity=trade_data['quantity'],
            price=trade_data['price'],
            cost_basis=trade_data.get('cost_basis', 0),
            realized_pnl=trade_data.get('pnl', 0),
            exchange_fee=trade_data.get('fee', 0),
            exchange=trade_data['exchange'],
            strategy=trade_data.get('strategy', 'MANUAL')
        )

        self.session.add(trade)
        self.session.commit()

        return trade.trade_id

    def get_trades_by_date(self, start_date, end_date):
        """Get trades for tax reporting"""
        return self.session.query(Trade).filter(
            Trade.timestamp >= start_date,
            Trade.timestamp <= end_date
        ).all()

    def generate_tax_report(self, year):
        """Generate annual tax report"""
        start = datetime(year, 1, 1)
        end = datetime(year, 12, 31, 23, 59, 59)

        trades = self.get_trades_by_date(start, end)

        total_proceeds = sum(t.price * t.quantity for t in trades if t.side == 'SELL')
        total_cost = sum(t.cost_basis for t in trades if t.side == 'SELL')
        total_fees = sum(t.exchange_fee for t in trades)
        net_gain = total_proceeds - total_cost - total_fees

        return {
            'year': year,
            'total_trades': len(trades),
            'total_proceeds': total_proceeds,
            'total_cost_basis': total_cost,
            'total_fees': total_fees,
            'net_gain_loss': net_gain
        }
```

**Action Items:**
```
[ ] Create exchanges.py with exchange adapters
[ ] Test connectivity to all exchanges
[ ] Create arbitrage.py with detection logic
[ ] Create risk.py with risk management
[ ] Create logger.py for trade logging
[ ] Run test trades with $1 amounts to verify everything works
```

---

## Phase 4: Paper Trading (Day 5-14)

### Step 11: Create Paper Trading Mode

#### Create paper_trader.py
```python
from arbitrage import ArbitrageDetector
from risk import RiskManager
from logger import TradeLogger
import time

class PaperTrader:
    def __init__(self):
        self.detector = ArbitrageDetector()
        self.risk = RiskManager(starting_capital=100)
        self.logger = TradeLogger()
        self.paper_balance = 100
        self.paper_trades = []

    def run(self, duration_hours=24):
        """Run paper trading simulation"""
        end_time = time.time() + (duration_hours * 3600)

        print(f"Starting paper trading for {duration_hours} hours...")
        print(f"Starting balance: ${self.paper_balance}")

        while time.time() < end_time:
            # Check for opportunities
            cross_opps = self.detector.find_cross_exchange_arb('BTC/USDT')
            tri_opps = self.detector.find_triangular_arb('binance')

            for opp in cross_opps + tri_opps:
                self._paper_execute(opp)

            # Wait before next check
            time.sleep(1)  # Check every second

        self._print_summary()

    def _paper_execute(self, opportunity):
        """Simulate trade execution"""
        # Calculate position size
        position = min(25, self.paper_balance * 0.25)

        # Check risk limits
        can_trade, reason = self.risk.can_trade(position, self.paper_balance)
        if not can_trade:
            print(f"Trade blocked: {reason}")
            return

        # Simulate execution with slippage
        spread = opportunity.get('spread', opportunity.get('profit', 0))
        slippage = 0.0005  # 0.05% slippage estimate
        fees = 0.002  # 0.2% round-trip fees

        net_profit_pct = spread - slippage - fees
        net_profit = position * net_profit_pct

        # Record result
        self.paper_balance += net_profit
        self.risk.record_trade(net_profit)
        self.risk.update_peak(self.paper_balance)

        trade_record = {
            'time': time.strftime('%Y-%m-%d %H:%M:%S'),
            'type': 'CROSS_EXCHANGE' if 'buy_exchange' in opportunity else 'TRIANGULAR',
            'gross_spread': spread,
            'net_profit_pct': net_profit_pct,
            'net_profit_usd': net_profit,
            'balance': self.paper_balance
        }
        self.paper_trades.append(trade_record)

        print(f"PAPER TRADE: {trade_record['type']} | "
              f"Spread: {spread:.4%} | "
              f"Net: ${net_profit:.2f} | "
              f"Balance: ${self.paper_balance:.2f}")

    def _print_summary(self):
        """Print paper trading summary"""
        print("\n" + "="*50)
        print("PAPER TRADING SUMMARY")
        print("="*50)
        print(f"Total trades: {len(self.paper_trades)}")
        print(f"Starting balance: $100.00")
        print(f"Ending balance: ${self.paper_balance:.2f}")
        print(f"Total P&L: ${self.paper_balance - 100:.2f}")
        print(f"Return: {(self.paper_balance - 100) / 100:.2%}")

        if self.paper_trades:
            wins = [t for t in self.paper_trades if t['net_profit_usd'] > 0]
            print(f"Win rate: {len(wins) / len(self.paper_trades):.1%}")

if __name__ == "__main__":
    trader = PaperTrader()
    trader.run(duration_hours=24)
```

### Step 12: Run Paper Trading

```bash
# Run for 24 hours minimum
python paper_trader.py
```

### Step 13: Validate Results

Before going live, confirm these metrics:

| Metric | Minimum Required | Your Result |
|--------|------------------|-------------|
| Win rate | > 75% | ___% |
| Avg profit per trade | > 0.15% | ___% |
| Max drawdown | < 10% | ___% |
| Trades per day | > 5 | ___ |
| System uptime | > 99% | ___% |

**Action Items:**
```
[ ] Run paper trading for minimum 7 days
[ ] Log all paper trades
[ ] Calculate win rate
[ ] Calculate average profit
[ ] Verify max drawdown stayed acceptable
[ ] Document any issues/bugs found
[ ] Fix any issues before going live
```

---

## Phase 5: Go Live (Day 14+)

### Step 14: Pre-Launch Checklist

```
[ ] All exchange APIs working
[ ] Database logging confirmed
[ ] Risk limits configured correctly
[ ] Paper trading results acceptable (>75% win rate)
[ ] Emergency stop procedure documented
[ ] Monitoring alerts set up
[ ] Backup of all code and config
```

### Step 15: Start with Minimal Capital

#### Create live_trader.py
```python
# Same structure as paper_trader.py but with real execution
# Start with these conservative settings:

LIVE_SETTINGS = {
    'max_trades_per_day': 5,      # Start slow
    'max_position_size': 10,       # $10 max per trade
    'enabled_strategies': ['cross_exchange'],  # Start with one strategy
    'enabled_pairs': ['BTC/USDT'],  # Start with one pair
    'dry_run': False,              # Set True to test without executing
}
```

### Step 16: Gradual Scale-Up Schedule

| Week | Active Capital | Max Trade Size | Strategies |
|------|---------------|----------------|------------|
| 1 | $25 | $10 | Cross-exchange only |
| 2 | $50 | $15 | + Triangular |
| 3 | $75 | $20 | + More pairs |
| 4 | $100 | $25 | Full system |

### Step 17: Set Up Monitoring

#### Basic monitoring with alerts
```python
# monitor.py
import requests

TELEGRAM_BOT_TOKEN = "your_bot_token"
TELEGRAM_CHAT_ID = "your_chat_id"

def send_alert(message):
    """Send Telegram alert"""
    url = f"https://api.telegram.org/bot{TELEGRAM_BOT_TOKEN}/sendMessage"
    data = {"chat_id": TELEGRAM_CHAT_ID, "text": message}
    requests.post(url, data=data)

# Call after each trade
send_alert(f"Trade executed: BTC +$2.50 | Balance: $127.50")
```

**Action Items:**
```
[ ] Verify pre-launch checklist complete
[ ] Enable live trading with $25
[ ] Monitor every trade for first 3 days
[ ] Gradually increase capital weekly
[ ] Set up Telegram/Discord alerts
[ ] Create daily review routine
```

---

## Phase 6: Ongoing Operations

### Daily Routine (5 minutes)

```
Morning check:
[ ] Review overnight trades
[ ] Check current balance vs expected
[ ] Verify no error alerts
[ ] Check exchange status pages

Evening check:
[ ] Review day's performance
[ ] Check daily P&L
[ ] Verify all positions closed (if day trading)
```

### Weekly Routine (30 minutes)

```
[ ] Review weekly P&L
[ ] Analyze win rate trend
[ ] Check for strategy drift
[ ] Rebalance funds across exchanges if needed
[ ] Update any expiring API keys
[ ] Review and adjust risk parameters if needed
```

### Monthly Routine (1 hour)

```
[ ] Generate monthly tax report
[ ] Review overall performance vs target (2x in 60 days)
[ ] Consider scaling up or adjusting strategies
[ ] Full system backup
[ ] Review exchange fee changes
[ ] Update dependencies (pip install --upgrade)
```

---

## Quick Reference: Emergency Procedures

### Stop All Trading Immediately
```python
# In your trading script
EMERGENCY_STOP = True  # Set this flag

# Or kill the process
# Ctrl+C in terminal
# Or: kill -9 <process_id>
```

### Close All Positions
```python
# Close all open positions at market
for exchange in exchanges:
    positions = exchange.fetch_positions()
    for pos in positions:
        exchange.create_market_order(
            pos['symbol'],
            'sell' if pos['side'] == 'long' else 'buy',
            pos['amount']
        )
```

### Contact Information
- Binance Support: https://www.binance.com/en/support
- Coinbase Support: https://help.coinbase.com
- OANDA Support: https://www.oanda.com/us-en/contact/

---

## Troubleshooting Common Issues

| Issue | Cause | Solution |
|-------|-------|----------|
| "Invalid API key" | Key not enabled or wrong | Regenerate API key |
| "Insufficient balance" | Funds not settled | Wait for deposit to clear |
| "Rate limit exceeded" | Too many requests | Add delays between calls |
| "Order too small" | Below minimum | Increase order size |
| "Connection timeout" | Network issue | Check internet, retry |

---

## Summary: Time to First Trade

| Phase | Duration | Cumulative |
|-------|----------|------------|
| Account setup & KYC | 1-3 days | Day 3 |
| Development setup | 1 day | Day 4 |
| Build components | 3-5 days | Day 9 |
| Paper trading | 7+ days | Day 16 |
| Go live (gradual) | 4 weeks | Day 44 |
| Full operation | Ongoing | Day 45+ |

**Minimum time to first real trade: ~14 days**
**Recommended time to full operation: ~45 days**

---

*Document Version: 1.0*
*Last Updated: January 2026*
*Reference: ARBITRAGE_VISUALIZATION_PLAN.md*
