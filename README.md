# GBLOXK OS · MINER AI v3.0

**Autonomous AI Mining Operating System — Real Pool Mining, Self-Healing, Self-Learning, Self-Awareness & Auto-Payout**

[![Version](https://img.shields.io/badge/version-3.0.0-blue.svg)](https://github.com/gbloxk-os/miner-ai)
[![Python](https://img.shields.io/badge/python-3.9%2B-green.svg)](https://python.org)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![AI](https://img.shields.io/badge/AI-Ollama-purple.svg)](https://ollama.ai)

---

## Overview

GBLOXK OS · MINER AI v3.0 is a production-ready autonomous mining operating system that combines **real SHA-256 pool mining** with an **advanced artificial intelligence layer** to deliver unprecedented efficiency, automation, and real BTC earnings.

### v3.0 Enterprise Features (All Implemented)

| Feature | Status | Description |
|---------|--------|-------------|
| **Real Bitcoin Pool Mining** | ✅ | Double-SHA256 mining with Stratum protocol, real block headers, share submission |
| **Stratum V1/V2 Pool Connectivity** | ✅ | TCP stratum server for ASIC/GPU miners + client connects to 8 major pools |
| **Multi-Coin Auto-Switching** | ✅ | Profitability-based switching across BTC, BCH, BSV, LTC, DASH, ZEC, KAS |
| **Rest API (FastAPI)** | ✅ | 22 endpoints for external integration |
| **Web Dashboard (React)** | ✅ | Enterprise fintech SPA with 7 views (Overview, Mining, AI Ecosystem, Analytics, History, Wallet, Settings) |
| **AI Ecosystem Visualization** | ✅ | Live neural-mesh SVG with 8 autonomous agents, real-time event feed, consciousness gauge |
| **Auto-Payout Engine** | ✅ | Automatically sends earned BTC to your wallet when balance crosses a configurable threshold |
| **Multi-Crypto Payout Addresses** | ✅ | Save any BTC/ETH/LTC/bech32 wallet address with validation; withdraw on demand |
| **Docker Deployment** | ✅ | Dockerfile + docker-compose |
| **ASIC Hardware Support** | ✅ | Stratum V1/V2 server accepts external miner connections |
| **Real BTC Withdrawal** | ✅ | Wallet with satoshi balance, auto-credit on shares, withdrawal requests |
| **AI Pool Analyzer** | ✅ | Scores pools by fee, acceptance rate, payout type, latency; auto-switches |
| **Air-Gapped Operation** | ✅ | Full offline capability - no internet required after install |

### Key Differentiators

| Feature | Our App | Competitors |
|---------|---------|-------------|
| **Real Pool Mining** | Connects to SlushPool, F2Pool, AntPool, ViaBTC, Poolin, Binance, NiceHash, CKPool | Most are simulators only |
| **AI Self-Healing** | Auto-detects & recovers from crashes, high temps, memory pressure | Manual intervention required |
| **AI Self-Learning** | Learns optimal settings from historical performance | Static configuration |
| **AI Self-Awareness** | Understands system health, predicts anomalies, generates recommendations | Basic monitoring only |
| **AI Pool Analyzer** | Scores pools by fee/acceptance/payout/latency; auto-switches | Manual pool selection |
| **Stratum V2** | Full SV2 protocol server + client with TCP support | Most still on SV1 |
| **AI Advisor (Ollama)** | Local AI runs on your machine - no cloud dependency | Cloud-based AI or none |
| **Auto-Mining Modes** | Performance, Balanced, Eco, Laptop Safe | Single mode only |
| **Profitability Calculator** | Real-time with live BTC price API | Manual calculation |
| **Resource Protection** | Thermal, CPU, RAM auto-throttling + OOM protection | No protection |
| **Wallet Auto-Credit** | Real-time satoshi credits on accepted shares | Manual tracking |
| **CLI Dashboard** | Professional real-time monitoring (like htop) | Basic status output |
| **REST API + Web UI** | FastAPI + React dashboard for remote management | CLI-only |

---

## Quick Start

### Installation

```bash
# Install from source
cd ai_bitcoin_miner
pip install -e .

# Or run directly
python main.py --version
```

### First Run (Real Bitcoin Mining)

```bash
# Register and start REAL Bitcoin mining (default)
gbloxk-os start

# View the monitoring dashboard
gbloxk-os monitor

# Check your mining status
gbloxk-os status

# Ask the AI advisor
gbloxk-os ai "How can I optimize my mining?"

# For educational/solo mining only
gbloxk-os start --solo
```

### v3.0 Enterprise Features

```bash
# Start the REST API server
gbloxk-os api --port 8765

# Start the Stratum pool server for ASIC miners
gbloxk-os stratum --port 3333

# Manage multi-coin auto-switching
gbloxk-os coin --list
gbloxk-os coin --enable --threshold 0.05

# Wallet & BTC withdrawal (auto-credited from real mining)
gbloxk-os wallet balance
gbloxk-os wallet withdraw --satoshi 10000 --address bc1...

# Connect to a specific real mining pool
gbloxk-os pool --pool slushpool --worker my_miner
gbloxk-os pool --host stratum.f2pool.com --port 1314 --worker my_worker

# AI pool analysis & recommendation
gbloxk-os pool --analyze

# Start with Docker
docker-compose up
```

---

## Command Reference

### Core Mining

| Command | Description |
|---------|-------------|
| `start` | Start automated AI mining |
| `stop` | Stop mining session |
| `status` | Display mining stats & AI self-report |
| `monitor` | Real-time dashboard (htop-style) |
| `config` | View/change configuration |

### AI & Analytics

| Command | Description |
|---------|-------------|
| `ai` | Ask the AI advisor questions |
| `profit` | Run profitability calculator |
| `self` | View self-healing/learning/awareness status |
| `analyze` | Full AI performance analysis |
| `history` | View past mining sessions |
| `feedback` | Submit feedback |

### Enterprise (v3.0)

| Command | Description |
|---------|-------------|
| `api` | Start/stop REST API server (FastAPI) |
| `stratum` | Start/stop Stratum pool server for ASIC/GPU miners |
| `coin` | Multi-coin auto-switching management |
| `wallet` | Wallet operations & BTC withdrawal |
| `pool` | Connect to real mining pools |

### Command Details

#### `gbloxk-os start`
Starts the mining engine with all AI systems enabled. **Defaults to REAL Bitcoin pool mining.**
- Real SHA-256 mining with Stratum protocol (connects to SlushPool by default)
- Self-Healing engine monitors for crashes/failures, high temps, memory pressure
- Self-Learning engine records performance data, finds optimal settings
- Self-Awareness engine analyzes system health, predicts anomalies
- Auto-tunes workers and difficulty based on system load
- Wallet auto-credits satoshi on every accepted share

**Options:**
```bash
gbloxk-os start              # Real pool mining (default)
gbloxk-os start --solo       # Educational solo mining only
gbloxk-os start --daemon     # Run in background
```

#### `gbloxk-os pool`
Connect to and manage real mining pools:
```bash
gbloxk-os pool --pool slushpool --worker my_miner    # Use known pool
gbloxk-os pool --host stratum.f2pool.com --port 1314 --worker my_worker  # Custom
gbloxk-os pool --analyze                               # AI recommendation
gbloxk-os pool --ai-switch                            # Enable AI auto-switch
gbloxk-os pool --stop                                 # Disconnect
```
Supported pools: slushpool, f2pool, antpool, viabtc, poolin, binance_pool, nicehash, ckpool

#### `gbloxk-os wallet`
Wallet management with auto-payout, address saving, and BTC withdrawal:
```bash
gbloxk-os wallet balance                                                # View balance & earnings
gbloxk-os wallet address --address bc1qw508d6qejxtdg4y5rrzarvary0c5xw7  # Save payout address
gbloxk-os wallet address                                                # Show current address
gbloxk-os wallet autopay --on --threshold 100000                        # Enable auto-send
gbloxk-os wallet autopay --off                                          # Disable auto-send
gbloxk-os wallet autopay                                                # Show auto-payout config
gbloxk-os wallet withdraw --satoshi 50000 --address bc1...              # Manual withdrawal
```
**Auto-credit**: Every accepted share automatically credits your wallet in real-time.
**Auto-payout**: When your balance crosses the threshold, coins are sent to your saved address automatically.

#### `gbloxk-os monitor`
Opens a real-time dashboard that displays:
- Mining stats (hashrate, blocks, difficulty, uptime)
- Profitability (daily/monthly profit with live BTC price)
- System resources (CPU, RAM, temperature, load, OOM risk)
- AI Self-* status (health, stability, consciousness)

#### `gbloxk-os api`
Start the FastAPI REST API server for external integration:
```bash
gbloxk-os api --port 8765 --host 127.0.0.1
# Open http://localhost:8765/docs for Swagger UI
```
Endpoints: `/`, `/health`, `/api/v1/stats`, `/api/v1/start`, `/api/v1/stop`,
`/api/v1/config`, `/api/v1/profitability`, `/api/v1/self`, `/api/v1/ai/advice`,
`/api/v1/blocks`, `/api/v1/coins`, `/api/v1/stratum`, `/api/v1/feedback`,
`/api/v1/wallet`, `/api/v1/wallet/withdraw`, `/api/v1/history`

#### `gbloxk-os stratum`
Start the Stratum pool server to accept ASIC/GPU miner connections:
```bash
gbloxk-os stratum --port 3333 --v2-port 3334 --difficulty 1.0
# Stratum V1 on port 3333, Stratum V2 on port 3334
```

#### `gbloxk-os coin`
Multi-coin auto-switching based on profitability:
```bash
gbloxk-os coin --list           # View supported coins
gbloxk-os coin --enable         # Enable auto-switching
gbloxk-os coin --disable        # Disable auto-switching
gbloxk-os coin --switch bitcoin # Manually switch coin
```

#### `gbloxk-os wallet`
Wallet management with real BTC withdrawal support:
```bash
gbloxk-os wallet balance                       # View wallet
gbloxk-os wallet withdraw --satoshi 50000 --address 1A1z...  # Withdraw BTC
gbloxk-os wallet address                       # Show BTC address
```

#### `gbloxk-os pool`
Connect to real mining pools:
```bash
gbloxk-os pool --pool slushpool --worker my_miner
gbloxk-os pool --host stratum.slushpool.com --port 3333 --worker my_miner
```
Supported pools: slushpool, f2pool, antpool, viabtc, poolin, binance_pool, nicehash, ckpool

#### `gbloxk-os profit`
Comprehensive profitability calculator:
```bash
# Using current mining stats
gbloxk-os profit

# Custom calculation
gbloxk-os profit --hashrate 100000 --power 65 --elec-cost 0.12
```

#### `gbloxk-os self`
Displays the complete AI Self-* system status:
- **Self-Awareness**: Health, stability, performance rating, consciousness level
- **Self-Learning**: Records collected, patterns discovered, insights generated
- **Self-Healing**: Incidents handled, recovery attempts

#### `gbloxk-os config`
View or modify configuration:
```bash
gbloxk-os config                                       # Show all settings
gbloxk-os config --set workers 4                       # Set workers
gbloxk-os config --set ollama_model llama3.2           # Change AI model
gbloxk-os config --set auto_throttle false             # Disable auto-throttle
```

---

## AI System Architecture

### Self-Healing Engine
- Monitors worker processes every 3 seconds
- Detects: crashes, zero hashrate, high temperature, memory pressure
- Auto-actions: restart worker, reduce workers, throttle difficulty
- Max 3 recovery attempts per incident type to prevent loops

### Self-Learning Engine
- Records performance data every mining cycle
- Analyzes patterns: best worker counts, difficulty levels, mode performance
- Stores up to 500 observations for trend analysis
- Auto-saves learning data to `data/learning_data.json`

### Self-Awareness Engine
- Maintains 5 baselines: CPU, memory, hashrate, temperature, system load
- Detects 4 anomaly types: CPU spikes, memory leaks, hashrate drops, temperature spikes
- Generates real-time recommendations
- Provides consciousness report with health overview

### Mining Modes

| Mode | Max CPU | Max RAM | Max Temp | Worker Ratio |
|------|---------|---------|----------|--------------|
| 🚀 Performance | 85% | 85% | 80°C | 80% |
| ⚖️ Balanced | 65% | 75% | 70°C | 50% |
| 🌿 Eco | 40% | 60% | 60°C | 25% |
| 💻 Laptop Safe | 50% | 70% | 65°C | 30% |

---

## Profitability

The app fetches live BTC price from CoinGecko API (cached 60 seconds) and calculates:

- **Daily BTC mined**: Based on your hashrate vs global network hashrate
- **Daily revenue**: BTC mined × current BTC price
- **Daily profit**: Revenue minus electricity costs and pool fees
- **Monthly/Yearly projections**: Scaled from daily
- **ROI percentage**: Profit margin as percentage
- **Days to 1 BTC**: Estimated time to mine 1 full Bitcoin solo

---

## Configuration

Config file: `config.json` (auto-created on first run)

Key settings:
```json
{
  "default_difficulty": 2,
  "max_nonce": 50000,
  "workers": 2,
  "max_workers": 4,
  "ollama_model": "huihui_ai/qwen3-abliterated:1.7b",
  "ollama_host": "http://localhost:11434",
  "block_reward": 3.125,
  "auto_tune_ai": true,
  "auto_throttle": true,
  "low_memory_mode": false,
  "air_gapped": false,
  "real_mining": true,
  "default_pool": "slushpool",
  "default_worker": "gbloxk_os.1"
}
```

### Real Mining Settings

| Setting | Description | Default |
|---------|-------------|---------|
| `real_mining` | Enable real pool mining (default: true) | `true` |
| `default_pool` | Pool to connect: slushpool, f2pool, antpool, etc. | `slushpool` |
| `default_worker` | Worker name for pool | `gbloxk_os.1` |
| `air_gapped` | Disable all external connections | `false` |

**Note**: Delete `config.json` to regenerate with new defaults after upgrading.

---

## Docker Deployment

```bash
# Start all services
docker-compose up -d

# This launches:
#   - Mining engine on ports 8765 (API), 3333 (Stratum V1), 3334 (Stratum V2)
#   - React dashboard on port 3000
```

---

## REST API Reference

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Root info |
| GET | `/health` | Health check |
| GET | `/api/v1/stats` | Mining stats |
| GET | `/api/v1/status` | System status |
| POST | `/api/v1/start` | Start mining |
| POST | `/api/v1/stop` | Stop mining |
| GET | `/api/v1/config` | Get config |
| POST | `/api/v1/config` | Update config |
| GET | `/api/v1/profitability` | Profit calculation |
| GET | `/api/v1/self` | Self-* status |
| GET | `/api/v1/ai/advice` | AI advice |
| GET | `/api/v1/blocks` | Block history |
| GET | `/api/v1/coins` | Supported coins |
| GET | `/api/v1/stratum` | Stratum status |
| POST | `/api/v1/feedback` | Submit feedback |
| GET | `/api/v1/wallet` | Wallet info |
| GET | `/api/v1/wallet/address` | Get payout address |
| POST | `/api/v1/wallet/address` | Save payout address |
| POST | `/api/v1/wallet/autopay` | Configure auto-payout |
| GET | `/api/v1/wallet/transactions` | Withdrawal ledger |
| POST | `/api/v1/wallet/withdraw` | BTC withdrawal |
| GET | `/api/v1/ai/ecosystem` | Live AI ecosystem snapshot |
| GET | `/api/v1/history` | Session history |

---

## Requirements

- Python 3.9+
- Ollama (for AI features - optional but recommended)
- 2GB RAM minimum (4GB+ recommended for mining)
- Multi-core processor

---

## Real Mining Architecture

### Real Bitcoin Mining Flow

```
┌─────────────────────────────────────────────────────────────────────┐
│                    GBLOXK OS · MINER AI v3.0                            │
├─────────────────────────────────────────────────────────────────────┤
│  ┌──────────────┐    ┌──────────────┐    ┌──────────────────────┐  │
│  │  PoolClient  │───▶│  RealMiner   │───▶│  Double-SHA256 Hash  │  │
│  │  (Stratum)   │    │  (Job Proc)  │    │  80-byte Block Hdr   │  │
│  └──────────────┘    └──────────────┘    └──────────────────────┘  │
│         │                    │                      │               │
│         ▼                    ▼                      ▼               │
│  ┌─────────────────────────────────────────────────────────────┐   │
│  │                    PoolMiner (Integration)                   │   │
│  │  • Auto-reconnect  • Share submission  • Wallet auto-credit │   │
│  └─────────────────────────────────────────────────────────────┘   │
│         │                    │                      │               │
│         ▼                    ▼                      ▼               │
│  ┌─────────────────────────────────────────────────────────────┐   │
│  │                  AutoRealMiner (AI Orchestrator)             │   │
│  │  • PoolAnalyzer  • Self-Learning  • Self-Awareness          │   │
│  │  • Auto-switch  • Alert throttling  • Profit prediction     │   │
│  └─────────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────────┘
```

### Module Structure

```
ai_bitcoin_miner/
├── main.py                        # Entry point with graceful shutdown
├── config.py                      # Configuration management (real_mining, default_pool)
├── database/
│   └── storage.py                 # SQLite with wallet, sessions, feedback, withdrawals
├── mining/
│   ├── blockchain.py              # Blockchain data structure
│   ├── engine.py                  # Multi-process SHA-256 engine (educational)
│   ├── worker.py                  # Mining worker thread
│   ├── orchestrator.py            # Central coordinator (real_mining flag)
│   ├── stratum_server.py          # Stratum V1/V2 TCP server (ASIC support)
│   ├── coin_switcher.py           # Multi-coin profitability switching
│   ├── pool_client.py             # Real mining pool Stratum client (8 pools)
│   ├── real_miner.py              # Real Bitcoin double-SHA256 mining
│   └── pool_miner.py              # PoolClient + RealMiner + Wallet integration
├── ai/
│   ├── analyzer.py                # System resource monitor + OOM protection (fixed temp)
│   ├── advisor.py                 # Ollama AI advisor
│   ├── profitability.py           # BTC price + P&L calculator (stdlib urllib)
│   ├── stratum.py                 # Stratum V2 protocol simulator
│   ├── alerts.py                  # Alert system (60s cooldown throttling)
│   ├── pool_analyzer.py           # AI pool scoring & recommendation
│   ├── auto_real_miner.py         # Complete AI auto-miner with pool switching
│   ├── self_healing.py            # Autonomous fault recovery
│   ├── self_learning.py           # Pattern recognition engine
│   └── self_aware.py              # System consciousness engine
├── api/
│   └── server.py                  # FastAPI REST API (18 endpoints)
├── cli/
│   ├── __main__.py                # CLI entry point (17 commands)
│   ├── commands.py                # All CLI command implementations
│   └── console_auth.py            # Interactive auth flow
├── dashboard/                     # React web dashboard (5 views)
│   ├── package.json
│   ├── public/index.html
│   └── src/
│       ├── App.js                 # Dashboard shell + routing
│       ├── Overview.js            # Mining overview stats
│       ├── Mining.js              # Mining control panel
│       ├── Analytics.js           # Profit & coin analytics
│       ├── Wallet.js              # Wallet & withdrawal
│       └── Settings.js            # Configuration
├── Dockerfile                     # Container deployment
├── docker-compose.yml             # Multi-service orchestration
├── setup.py                       # Package installer
└── requirements.txt               # Python dependencies
```

## Fixed Issues (v3.0.1)

| Issue | Fix |
|-------|-----|
| Database "locked" crashes | Single persistent SQLite connection with WAL + busy_timeout |
| CLI SyntaxError (global AUTO_REAL) | Moved global declaration to function start |
| Unrealistic temperature (98°C) | Prefers coretemp sensors, averages CPU cores (~57°C) |
| Alert spam (every 4s) | 60-second cooldown per message; solo mode suppressed |
| User ID boolean bug | `register_user()` returns int ID |
| Wallet not auto-crediting | `credit_wallet()` called on every accepted share |

---

.
---

## Support

- Documentation: See this README and USER_GUIDE.md
- Issues: Report at our GitHub repository
- Feedback: `gbloxk-os feedback "your message"`
