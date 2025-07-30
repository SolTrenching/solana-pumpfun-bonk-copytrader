<img width="979" height="370" alt="image" src="https://github.com/user-attachments/assets/43369374-69b6-430e-b066-7b18fb2c0565" />
<img width="281" height="242" alt="image" src="https://github.com/user-attachments/assets/51d044fc-04fe-4530-8767-df85dba06fea" />



# solana-pumpfun-bonk-copytrader
Solana Pump.fun &amp; BONK Copy Trading Bot – Automatically copy any wallet’s trades on the hottest Solana tokens. Fast, secure, fully configurable, with free Helius RPC support. Closed source, real-time, and beginner friendly.


# Pump.fun Copy Trading Bot

A Solana copy trading bot that monitors a target wallet and automatically copies their Pump.fun & BONK buy/sell transactions using a free Helius RPC endpoint.

## 🎯 Target Wallet
This bot is configured to monitor and copy trades.

## ⚠️ Important Disclaimers

**This bot is for educational purposes only and should not be considered financial advice.**

- Trading bots can be risky and may result in financial loss
- Always do your own research before using trading bots
- Start with small amounts and test thoroughly
- Transactions on-chain are irreversible

## 🚀 Features

- ✅ Monitors target wallet for Pump.fun & BONK buy/sell transactions
- ✅ Automatically copies trades above minimum threshold
- ✅ Uses free Helius RPC (no paid gRPC required)
- ✅ Configurable trade amounts and limits
- ✅ Test mode for safe testing
- ✅ Comprehensive logging
- ✅ Real-time transaction monitoring
- ✅ Graceful error handling

## 📋 Prerequisites

- Node.js (v16 or higher)
- A Solana wallet with SOL balance
- Free Helius RPC API key
- Basic understanding of Solana and DeFi

## 🛠️ Setup

### 1. Download app from Releases

Rename `Default.env` to `.env`

### 2. Environment Configuration

Edit `.env` file:

```env
# Get free API key from https://helius.dev
# Solana RPC endpoint (free Helius endpoint)
# SOLANA_RPC=https://mainnet.helius-rpc.com/?api-key=YOUR_API_KEY
SOLANA_RPC=https://api.mainnet-beta.solana.com

# Your wallet secret key
SECRET_KEY=

# Target wallet to copy (the wallet you specified)
TARGET_WALLET=

MIN_SOL_AMOUNT=
COPY_SOL_AMOUNT=
MAX_SOL_AMOUNT=

# Test mode - set to false for real trading
TEST_MODE=false

# Polling interval in milliseconds
POLLING_INTERVAL=500
```

### 3. Get Your Private Key

To get your wallet's private key:

**Base58 String**
```bash
# From Phantom/Solflare wallet: Settings → Export Private Key
```


### 4. Fund Your Wallet

Make sure your bot wallet has enough SOL for:
- Transaction fees
- Copy trading amounts
- Buffer for multiple trades

Recommended minimum: 0.1 SOL for testing

## 🏃‍♂️ Running the Bot

### Test Mode (Recommended First)

The bot will:
1. ✅ Validate configuration
2. ✅ Connect to Solana network
3. ✅ Monitor target wallet
4. ✅ Simulate copy trades (no real transactions)

### Live Trading Mode

1. Set `TEST_MODE=false` in `.env`

## 📊 How It Works

1. **Monitoring**: Polls target wallet every 5 seconds for new transactions
2. **Analysis**: Checks if transaction is a buy above minimum threshold
3. **Execution**: If criteria met, executes copy trade with configured amount

## 🔧 Configuration Options

| Setting | Description | Default |
|---------|-------------|---------|
| `MIN_SOL_AMOUNT` | Minimum target trade to copy
| `COPY_SOL_AMOUNT` | Our trade amount
| `MAX_SOL_AMOUNT` | Maximum trade limit
| `TEST_MODE` | Enable simulation mode
| `POLLING_INTERVAL` | Check frequency (ms)

## 🛡️ Safety Features

- **Test Mode**: Simulate trades without spending money
- **Amount Limits**: Configurable min/max trade amounts  
- **Error Handling**: Graceful error recovery
- **Transaction Validation**: Verify transactions
- **Balance Checking**: Monitor wallet balance
- **Signature Tracking**: Prevent duplicate processing

### Common Issues

**"Missing environment variable"**
- Check `.env` file exists and has all required variables

**"Invalid TARGET_WALLET address"**
- Verify wallet address is correct Solana public key

**"Error connecting to RPC"**
- Check Helius API key is valid
- Verify internet connection

**"Insufficient balance"**
- Add more SOL to your wallet
- Check wallet address is correct

**"No transactions found"**
- Target wallet may not be trading
- Check polling interval settings

## 🔗 Useful Links

- [Helius RPC](https://helius.dev) - Free Solana RPC
- [Pump.fun](https://pump.fun) - Trading platform  
- [Solscan](https://solscan.io) - Transaction explorer
- [Jupiter](https://jup.ag) - Swap aggregator

## ⚖️ Legal

- This software is for educational purposes only
- No warranty or guarantee of profits
- Use at your own risk
- Comply with local regulations
- Authors not responsible for losses

## 🤝 Support

For issues or questions:
1. Check this README
2. Verify configuration
3. Test with small amounts first

---

**Remember: Only trade with funds you can afford to lose!**
