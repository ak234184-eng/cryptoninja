# CryptoNinja Trading Bot

CryptoNinja is a sophisticated, modular cryptocurrency futures trading bot that integrates with CoinDCX exchange. The system leverages artificial intelligence and machine learning to analyze market conditions, select optimal trading strategies, and execute trades with sophisticated risk management.

## Features

### 🔗 Exchange Integration
- Seamless integration with CoinDCX API
- Real-time market data fetching
- Robust error handling and retry logic
- Secure API key management

### 📊 Indicator Engine
- Complete suite of technical indicators:
  - Oscillators: RSI, Stochastic, CCI, ADX, MACD, Momentum, Awesome Oscillator
  - Moving Averages: SMA & EMA (10, 20, 30, 50, 100, 200)
  - Volume indicators for enhanced accuracy
- Indicator consensus mechanism
- Volume spike detection

### 🧠 Strategy Engine
- Multiple trading strategies:
  - Trend Following
  - Mean Reversion
  - Breakout
  - Scalping
  - And more...
- Dynamic strategy selection based on market conditions
- Strategy performance tracking
- Parameter optimization

### 🛡️ Risk Management
- Isolated margin mode for controlled risk
- Configurable leverage, SL/TP, and capital allocation
- Global circuit breaker for drawdown protection
- Comprehensive error handling and recovery

### 📝 Logging System
- Detailed CSV logs for:
  - Trades
  - Errors
  - Strategy usage
  - Account snapshots
- Structured data for analysis and auditing

### 🤖 AI/ML Intelligence (Optional)
- Signal prediction using LSTM/Transformer models
- Sentiment analysis of news and social media
- Anomaly detection for unusual market conditions
- Reinforcement learning for strategy optimization

## Installation

### Prerequisites
- Python 3.9 or higher
- pip (Python package manager)
- Git

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/cryptoninja.git
   cd cryptoninja
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create necessary directories:
   ```bash
   mkdir -p logs reports
   ```

5. Configure the bot:
   - Edit `config/default.json` with your settings
   - Add your CoinDCX API key and secret

## Usage

### Running the Bot

```bash
# Run with default configuration
python src/main.py

# Run with custom configuration
python src/main.py --config path/to/your/config.json
```

### Generating Performance Reports

```bash
# Generate performance report
python src/main.py --report

# Generate report in custom directory
python src/main.py --report --report-dir path/to/reports
```

### Configuration

The bot is configured using a JSON file. The default configuration is in `config/default.json`. You can create your own configuration file and specify it with the `--config` option.

Key configuration sections:

- **API Credentials**: Set your CoinDCX API key and secret
- **Trading Symbols**: List of cryptocurrency pairs to trade
- **Timeframes**: Trading timeframe and update intervals
- **Indicators**: Configure technical indicators
- **Strategies**: Enable/disable strategies and set parameters
- **Risk Management**: Set risk parameters like max drawdown and position sizing
- **AI/ML**: Enable/disable AI features (requires additional setup)

## Project Structure

```
cryptoninja/
├── config/                      # Configuration files
│   └── default.json             # Default configuration
├── logs/                        # Log files
├── reports/                     # Performance reports
├── src/                         # Source code
│   ├── ai/                      # AI/ML intelligence module
│   ├── exchange/                # Exchange integration module
│   ├── indicators/              # Indicator engine module
│   ├── logging/                 # Logging system module
│   ├── risk/                    # Risk management module
│   ├── strategies/              # Strategy engine module
│   ├── bot.py                   # Trading bot core
│   └── main.py                  # Application entry point
└── README.md                    # This file
```

## Safety and Disclaimer

**IMPORTANT**: This trading bot is provided for educational and research purposes only. Cryptocurrency trading involves significant risk and you can lose money. Always start with small amounts and test thoroughly before committing significant capital.

- Always use testnet mode first
- Start with small position sizes
- Monitor the bot regularly
- Understand that no trading strategy guarantees profits

## License

This project is licensed under the MIT License - see the LICENSE file for details.
