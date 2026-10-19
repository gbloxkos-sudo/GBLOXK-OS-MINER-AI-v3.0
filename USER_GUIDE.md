# GBLOXK OS · MINER AI - Complete User Guide

## Professional AI-Powered Bitcoin Mining Platform

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [Installation](#2-installation)
3. [Quick Start](#3-quick-start)
4. [Command Reference](#4-command-reference)
5. [AI System Guide](#5-ai-system-guide)
6. [Mining Modes](#6-mining-modes)
7. [Configuration](#7-configuration)
8. [Monitoring & Analytics](#8-monitoring--analytics)
9. [Self-* System](#9-self--system)
10. [Profitability](#10-profitability)
11. [Best Practices](#11-best-practices)
12. [Troubleshooting](#12-troubleshooting)
13. [API Reference](#13-api-reference)
14. [Security](#14-security)

---

## 1. Introduction

GBLOXK OS · MINER AI is a **production-grade Bitcoin mining platform** that combines traditional SHA-256 proof-of-work mining with advanced artificial intelligence. It features three proprietary AI systems:

### The Three AI Pillars

#### 🩹 Self-Healing Engine
The Self-Healing engine is an autonomous fault-detection and recovery system that continuously monitors the mining process. It detects crashes, zero-hashrate conditions, temperature spikes, and memory pressure - then automatically takes corrective action (restart workers, reduce load, throttle difficulty) without human intervention.

**Key Metrics:**
- Monitoring interval: 3 seconds
- Recovery attempts per incident: Max 3
- Recovery actions: 6 types (restart, reinitialize, adjust, throttle, reduce, log)

#### 📚 Self-Learning Engine
The Self-Learning engine is a pattern recognition system that records mining performance data and identifies optimal configurations over time. It tracks worker counts, difficulty levels, mode performance, and time-of-day patterns to build a knowledge base of what works best for your specific hardware.

**Key Metrics:**
- Record capacity: 500 observations
- Analysis interval: 60 seconds
- Pattern types: 4 (worker count, difficulty, mode, time-of-day)
- Data persistence: `data/learning_data.json`

#### 🧠 Self-Awareness Engine
The Self-Awareness engine is a system consciousness layer that understands the overall health state of the mining operation. It maintains 5 baseline metrics, detects 4 anomaly types (CPU spikes, memory leaks, hashrate drops, temperature spikes), and generates real-time health assessments and recommendations.

**Awareness States:**
- `AWAKE` - Normal operation, system responsive
- `SLEEPING` - System under heavy load or degraded
- Health levels: `excellent` → `good` → `fair` → `monitoring` → `critical`

---

## 2. Installation

### Prerequisites

- **Python 3.9+** (3.11 recommended)
- **Ollama** (for AI features - optional but recommended)
- **4GB RAM** minimum (8GB recommended)
- **Multi-core processor**

### Quick Install

```bash
# Clone or navigate to the project
cd gbloxk-os-miner-ai

# Install dependencies
pip install -r requirements.txt

# Make the command available system-wide (choose one method)
# Method 1: Symlink (recommended for development)
chmod +x main.py
ln -sf "$(pwd)/main.py" ~/.local/bin/gbloxk-os

# Method 2: Add alias to .bashrc
echo "alias gbloxk-os='python3 $(pwd)/main.py'" >> ~/.bashrc
source ~/.bashrc

# Verify installation
gbloxk-os --version
```

### Ollama Setup (For AI Features)

```bash
# Install Ollama
curl -fsSL https://ollama.ai/install.sh | sh

# Pull a model (choose one)
ollama pull llama3.2          # Fast, good for most tasks
ollama pull qwen3:1.7b        # Lightweight
ollama pull mistral           # Balanced

# Configure the app to use your model
gbloxk-os config --set ollama_model llama3.2
```

---

## 3. Quick Start

### First Mining Session

```bash
# Step 1: Register an account (first time)
gbloxk-os start
# Follow the registration prompt

# Step 2: Start mining
gbloxk-os start

# Step 3: View the real-time dashboard
gbloxk-os monitor

# Step 4: Check your stats
gbloxk-os status

# Step 5: Stop mining when done
gbloxk-os stop
```

### Your First AI Consultation

```bash
# Ask the AI advisor about optimization
gbloxk-os ai "What difficulty should I use for my 4-core CPU?"

# Get a full performance analysis
gbloxk-os analyze

# Check AI self-* system health
gbloxk-os self
```

---

## 4. Command Reference

### Global Options

| Option | Description |
|--------|-------------|
| `--version` | Show version and exit |
| `--help` | Show help message and exit |

### Command Details

#### `gbloxk-os start`
Starts the mining engine with all AI systems.
```bash
gbloxk-os start              # Interactive mode
gbloxk-os start --daemon     # Background mode (experimental)
```
On first run, you'll be prompted to register or login.

#### `gbloxk-os stop`
Stops the active mining session and saves statistics to the database.

#### `gbloxk-os status`
Displays comprehensive mining status including:
- Current mining stats (hashrate, blocks, difficulty, uptime)
- System resources (CPU, RAM, temperature)
- AI Self-* health report
- Profitability calculations
- Last 10 session history (if no active session)

#### `gbloxk-os monitor`
Opens a real-time, auto-refreshing dashboard (like `htop` for mining). Displays:
- 📊 Mining statistics panel
- 💻 System resources panel
- 🧠 AI Self-* status panel
- Live BTC price and profitability

Press `Ctrl+C` to exit the dashboard.

#### `gbloxk-os config`
View or modify configuration settings.
```bash
gbloxk-os config                          # Show all settings
gbloxk-os config --set workers 8          # Set worker count
gbloxk-os config --set default_difficulty 3  # Set difficulty
gbloxk-os config --set ollama_model llama3.2  # Change AI model
gbloxk-os config --get workers            # Show single value
```

#### `gbloxk-os ai`
Consult the AI advisor.
```bash
gbloxk-os ai "How can I optimize?"        # Ask a specific question
gbloxk-os ai                               # Run performance analysis
```

#### `gbloxk-os profit`
Run the profitability calculator.
```bash
gbloxk-os profit                          # Use current mining stats
gbloxk-os profit --hashrate 1000000 --power 65 --elec-cost 0.12
gbloxk-os profit --hashrate 500000000 --power 3250 --reward 3.125
```

Parameters:
| Option | Default | Description |
|--------|---------|-------------|
| `--hashrate` | Current | Hash rate in H/s |
| `--power` | 65 | Power consumption in watts |
| `--elec-cost` | 0.12 | Electricity cost $/kWh |
| `--pool-fee` | 2.0 | Mining pool fee in % |
| `--reward` | Config | Block reward in BTC |

#### `gbloxk-os self`
Display the complete AI Self-* system status report including Self-Healing incidents, Self-Learning patterns, and Self-Awareness consciousness report.

#### `gbloxk-os analyze`
Run a comprehensive AI performance analysis. Uses Ollama to analyze current mining metrics and provide optimization recommendations.

#### `gbloxk-os history`
View the last 20 mining sessions with duration, blocks found, hash rate, and status.

#### `gbloxk-os feedback <message>`
Submit feedback to the development team.

---

## 5. AI System Guide

### AI Advisor

The AI Advisor uses Ollama to provide intelligent recommendations. It analyzes:
- Current hashrate and mining efficiency
- System resource utilization
- Historical performance data
- Self-awareness health reports

**Example queries:**
```
gbloxk-os ai "What's the optimal worker count for my system?"
gbloxk-os ai "How can I reduce power consumption while mining?"
gbloxk-os ai "Analyze my mining performance and suggest improvements"
gbloxk-os ai "Should I use a different difficulty level?"
```

### AI Auto-Mining

When `auto_tune_ai = true` in config, the system automatically:
1. Adjusts worker count based on CPU/RAM availability
2. Sets optimal difficulty based on system capacity
3. Throttles mining when temperature exceeds thresholds
4. Records observations for the Self-Learning engine
5. Feeds data to the Self-Awareness engine for anomaly detection

---

## 6. Mining Modes

The system supports four mining modes, automatically selected or manually configured:

| Mode | Max CPU | Max RAM | Max Temp | Worker Ratio | Best For |
|------|---------|---------|----------|--------------|----------|
| 🚀 **Performance** | 85% | 85% | 80°C | 80% | Dedicated desktops |
| ⚖️ **Balanced** | 65% | 75% | 70°C | 50% | Daily-use computers |
| 🌿 **Eco** | 40% | 60% | 60°C | 25% | Energy saving |
| 💻 **Laptop Safe** | 50% | 70% | 65°C | 30% | Laptops |

**How mode affects behavior:**
- **Worker count** = Total Cores × Worker Ratio × Throttle Factor
- **Difficulty** = Auto-calculated from available resources
- **Temperature threshold** = Triggers automatic throttling
- **CPU/Memory limits** = Prevents system overload

---

## 7. Configuration

Configuration is stored in `config.json` in the project root.

### Key Settings

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| `default_difficulty` | int | 4 | Mining difficulty (1-10) |
| `max_nonce` | int | 100000 | Nonce search range |
| `workers` | int | 4 | Number of parallel workers |
| `ollama_model` | str | qwen3-abliterated:1.7b | AI model name |
| `ollama_host` | str | localhost:11434 | Ollama server URL |
| `block_reward` | float | 6.25 | BTC reward per block |
| `auto_tune_ai` | bool | true | Enable AI auto-tuning |
| `auto_save_interval` | int | 30 | Stats save interval (seconds) |

---

## 8. Monitoring & Analytics

### Real-Time Dashboard

The `gbloxk-os monitor` command provides an `htop`-style dashboard with four panels:

**📊 Mining Stats Panel:**
- Hash Rate (formatted with units: H/s, KH/s, MH/s)
- Blocks Found (total in current session)
- Current Difficulty
- Total Hashes Computed
- Uptime (formatted: h/m/s)
- Live BTC Price (from CoinGecko API)
- Chain Length
- Total Shares Submitted
- Acceptance Rate (%)
- Active Workers
- Daily/ Monthly Profit

**💻 System Resources Panel:**
- CPU Usage (%)
- Memory Usage (%)
- Temperature (°C)
- Available RAM (GB)
- Logical / Physical Cores
- Load Average (1m, 5m, 15m)

**🧠 AI Self-* Panel:**
- System Health (excellent/good/fair/critical)
- Stability Score (%)
- Consciousness Level (AWAKE/SLEEPING)
- Anomaly Count
- Auto-Healing Incidents
- Learning Patterns Found
- Records Collected

### Session History

View past mining sessions with:
```bash
gbloxk-os history
```

Displays: Date, Duration, Difficulty, Blocks Found, Total Hashes, Avg Hash Rate, Status

---

## 9. Self-* System

### Self-Healing Incident Types

| Incident Type | Trigger | Auto-Action |
|---------------|---------|-------------|
| `worker_crash` | Worker process stops | Automatic restart |
| `zero_hashrate` | No hash for 30+ seconds | Reinitialize worker |
| `forced_pause` | System pressure detected | Reduce workers |
| `high_temperature` | Temp > threshold | Throttle workers |
| `memory_pressure` | RAM > 85% | Reduce workers aggressively |

### Self-Learning Patterns

After sufficient runtime, the system identifies:
- **Best worker count** for your hardware
- **Optimal difficulty** for current conditions
- **Best performing mode** (performance/balanced/eco/laptop-safe)
- **Time-of-day patterns** for performance variations
- **Performance trends** (improving/declining)

### Self-Awareness Baselines

The system maintains dynamic baselines for:
- CPU usage (normal range for your hardware)
- Memory usage (typical consumption)
- Hashrate (expected output)
- Temperature (operating range)
- System load (average load patterns)

---

## 10. Profitability

### Live Calculation

The profitability calculator fetches live BTC price from CoinGecko API and calculates:

- **BTC Price**: Current market price (cached 60 seconds)
- **Network Hashrate**: Global Bitcoin network hashrate (624 EH/s default)
- **Daily BTC**: Your share of daily block rewards
- **Daily Revenue**: BTC × Price
- **Daily Costs**: Power consumption × Hours × Rate
- **Net Profit**: Revenue - Costs (daily/monthly/yearly)
- **ROI**: Profit margin as percentage
- **Days to 1 BTC**: Estimated time to mine 1 BTC solo

### Interpretation

**Positive values indicate profit; negative values indicate loss.**
CPU mining of Bitcoin is primarily educational - real profitability requires ASIC hardware. However, the AI optimization system and learning algorithms work identically for:
- Educational blockchain learning
- Mining strategy testing
- AI optimization research
- Alternative cryptocurrency mining

---

## 11. Best Practices

### For Laptops

```bash
# Limit resource usage
gbloxk-os config --set workers 2
gbloxk-os config --set default_difficulty 2
gbloxk-os config --set auto_tune_ai true

# Monitor temperature closely
gbloxk-os monitor
```

### For Desktops

```bash
# Moderate usage
gbloxk-os config --set workers 4
gbloxk-os config --set default_difficulty 4

# Performance mode
gbloxk-os config --set workers 8
gbloxk-os config --set default_difficulty 6
```

### For Server/Headless

```bash
# Maximize output
gbloxk-os config --set workers $(nproc)
gbloxk-os config --set default_difficulty 6
gbloxk-os config --set max_nonce 500000
gbloxk-os start
```

### Regular Maintenance

- ✅ **Daily**: Run `gbloxk-os monitor` to check system health
- ✅ **Weekly**: Run `gbloxk-os self` to review AI insights
- ✅ **Monthly**: Run `gbloxk-os analyze` for comprehensive optimization
- ✅ **Quarterly**: Review `gbloxk-os history` for performance trends
- ✅ **As needed**: `gbloxk-os feedback "suggestion"` to help improve

---

## 12. Troubleshooting

### Common Issues and Solutions

| Issue | Cause | Solution |
|-------|-------|----------|
| `ModuleNotFoundError` | Missing dependencies | `pip install -r requirements.txt` |
| AI not responding | Ollama not running | Start Ollama: `ollama serve` |
| High CPU usage | Too many workers | Reduce workers: `gbloxk-os config --set workers 2` |
| Memory warnings | System overload | Switch to Eco or Laptop Safe mode |
| No blocks found | Difficulty too high | Reduce difficulty: `gbloxk-os config --set default_difficulty 2` |
| `gbloxk-os: command not found` | Not in PATH | Run `source ~/.bashrc` or use `python3 main.py` |
| Database errors | Corrupted DB | Delete `data/miner.db` and restart |
| Monitor not updating | No active session | Start mining first: `gbloxk-os start` |

### Logs

Logs are stored at `~/.gbloxk_os/logs/miner.log`. Check logs for detailed error information.

---

## 13. API Reference

### Internal APIs

The application exposes its functionality through a modular Python API:

```python
from config import AppConfig
from database.storage import DatabaseManager
from mining.orchestrator import MiningOrchestrator

# Initialize
config = AppConfig.load()
db = DatabaseManager(config.db_path)

# Login
uid = db.authenticate_user("username", "password")

# Start orchestrator
orch = MiningOrchestrator(config, db, uid)
orch.start_mining()

# Get stats
stats = orch.get_stats()

# Get AI analysis
analysis = orch.ai_analyze()

# Get self-* status
self_status = orch.get_self_status()

# Profitability
profit = orch.get_profitability()

# Stop
orch.stop_mining()
```

### External API Dependencies

| API | Endpoint | Purpose | Fallback |
|-----|----------|---------|----------|
| CoinGecko | `api.coingecko.com/api/v3/simple/price?ids=bitcoin` | Live BTC price | Cached value ($65,000 default) |
| Ollama | `localhost:11434/api/chat` | AI inference | Informative error message |

---

## 14. Security

### Authentication
- Passwords hashed with SHA-256
- SQLite database with WAL mode
- Local storage - no data leaves your machine

### AI Privacy
- All AI inference runs **locally** via Ollama
- No data sent to external AI services
- No telemetry or analytics collection

### Network Security
- Only outbound connection: CoinGecko API (BTC price)
- Configurable Ollama host (default: localhost)
- No open ports or network services

### Data Storage
- SQLite database in project `data/` directory
- Learning data in `data/learning_data.json`
- Logs in `~/.gbloxk_os/logs/`
- All data stays on your machine

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 2.0.0 | 2026 | AI Self-* system, CLI dashboard, profitability calculator |
| 1.0.0 | 2025 | Initial release with basic mining and AI advisor |

---

*Documentation version 2.0.0 - © 2026 GBLOXK OS · MINER AI Team*
