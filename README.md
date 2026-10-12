# ZENTHEA PERPETUALS COCKPIT 📈
### Autonomous Perpetual Futures Execution Engine // Real-Time Cyberpunk Terminal
**Principal:** Puzzled Programmer  
**License:** Commercial Proprietary — Verified Distribution Package

---

## 🚀 Official Releases & Distribution Packages

Welcome to the official public distribution portal for **Zenthea Perpetuals Cockpit**. This repository provides signed, standalone Windows binaries and official release archives for licensed users.

> [!NOTE]
> Source code is proprietary and maintained in an isolated private research environment. This repository hosts pre-compiled binaries, changelogs, and update packages only.

---

## 📥 Latest Release

### [v1.0.0 — Autonomous Perpetual Futures Execution Engine & Cyberpunk Cockpit (Windows x64)](https://github.com/bryangarces-ai/perp-cockpit-releases/releases/tag/v1.0.0)

| Package | Format | Description |
| :--- | :--- | :--- |
| **[ZentheaPerp-v1.0.0-Windows.zip](https://github.com/bryangarces-ai/perp-cockpit-releases/releases/download/v1.0.0/ZentheaPerp-v1.0.0-Windows.zip)** | `.zip` | **Full Package (Recommended):** Standalone executable, documentation, setup guide, configuration templates, and 1-click launcher |
| **[ZentheaPerpCockpit.exe](https://github.com/bryangarces-ai/perp-cockpit-releases/releases/download/v1.0.0/ZentheaPerpCockpit.exe)** | `.exe` | Standalone binary (drop-in update for existing folders with auto-reconciling `.env`) |

---

## 🌟 What's New in v1.0.0

* **Single-Port Unified Cockpit (`http://localhost:8890`):**
  * Embedded Angular 19+ Cyberpunk Cockpit directly served from FastAPI without requiring Node.js, npm, or Python on the client PC.
  * Real-time Lightweight Charts, S/R Donchian bands, order flow metrics, and live positions monitor.
* **The 6-Gate Tactical Strike Radar (`pipeline-hud.component.ts`):**
  * No order is ever dispatched unless all 6 gates pass concurrently:
    1. `Signal Setup`: RSI $\le 38$ / $\ge 62$ + Trend Alignment.
    2. `Volume Fuel`: $\ge 0.60\times\text{Med}_{20}$ volume barrier.
    3. `Regime Guard`: $\text{ADX} \ge 20$ (filters chop and range traps).
    4. `S/R Runway`: Asymmetric $1.8:1$ to $2.5:1$ RRR clearance to opposing Donchian boundary.
    5. `JEV AI Conviction`: $\ge 65\%$ System One neural conviction score.
    6. `Portfolio Barrier`: Max 2 concurrent positions cap and pre-flight free margin check at 3x cross leverage.
* **Native OKX OCO Bracket Algo Orders (`backend/core/exchange.py`):**
  * Bracket orders submitted directly via OKX v5 algo endpoints (`ordType: "oco"`, `tpTriggerPxType: "mark"`, `slTriggerPxType: "mark"`).
  * Exits execute natively on OKX high-frequency matching engine—zero local polling exit delay.
* **Ironclad Stop-Loss Placement Guarantee ("Never Hold Naked" Policy):**
  * Multi-attempt Stop Loss placement with exponential backoff (up to 3 retries).
  * Actively queries matching engine (`verify_sl_active`) to confirm active exchange stops.
  * Fail-safe emergency abort: immediately market-flattens the position if the exchange rejects or fails to register stops.
* **Dynamic Break-Even Locking:**
  * Automatically shifts Stop Loss to entry price + fees when floating profit reaches $1.0\times$ risk distance, locking in risk-free runners.
* **Dual-Environment Architecture (`DEMO` ↔ `LIVE`):**
  * One-click switching between OKX Simulated Trading (~$5,100 USDT) and OKX Production API.
  * Hard auto-disarm safety interlock: switching environments unconditionally disarms the bot to prevent unintended live execution.
* **5-Pair Dynamic Multi-Asset Watchlist:**
  * Active by default: `SOL/USDT` (EMA Trend), `DOGE/USDT` (Dual-Alpha), `XAU/USDT` (Synthetic Gold).
  * High bankroll toggles: `BTC/USDT` (0.01 lot size), `ETH/USDT` (0.1 lot size).

---

## ⚡ Quick Start Guide (New Users)

### Step 1: Download & Extract
1. Download **`ZentheaPerp-v1.0.0-Windows.zip`** from the table above.
2. Extract the zip file into a folder of your choice (e.g. `C:\Trading\ZentheaPerp\`).

### Step 2: Activate Your License
1. Double-click **`run_cockpit.bat`** (or `ZentheaPerpCockpit.exe`).
2. When prompted in the terminal, enter your license key provided by **Puzzled Programmer**:
   ```text
   Format: ZENTHEA-XXXX-XXXX-XXXX-XXXX
   ```
3. The engine activates securely with the cloud server and binds to your PC.

### Step 3: Configure Your Exchange Credentials
* **Option A (In-App Guided Wizard):** On first launch, the terminal wizard asks:
  ```
  Would you like to enter your credentials now? [Y/n]
  ```
  Press **Enter** and paste your OKX API Key, Secret, and Passphrase. The engine tests your connection live with OKX and saves everything automatically!
* **Option B (Manual Setup):** Rename `.env.example` to `.env` and fill in your keys.

### Step 4: Launch Web Cockpit
1. In the terminal menu, press **`1`** (or Enter):
   ```
   [1] Launch Cyberpunk Cockpit GUI
   ```
2. Your default web browser will automatically open right into the trading cockpit at:
   ```
   http://localhost:8890
   ```
3. In the header HUD, click **`[🟢 ARM]`** to enable autonomous scanning.

---

## 🔄 How to Update Your Application

When updating to a future version:

1. Close the running `ZentheaPerpCockpit.exe` application.
2. Download the latest **`ZentheaPerp-vX.X.X-Windows.zip`**.
3. Drag the new `ZentheaPerpCockpit.exe` into your existing folder and choose **Replace**.
4. Double-click `run_cockpit.bat`:
   * **Your exchange credentials (`.env`) are permanently preserved.**
   * **Your strategy configurations (`config/`) are permanently preserved.**
   * **Your trade ledger and closed PnL history (`data/`) are automatically preserved!**

---

## 🏛️ Core Architectural Safeguards

1. **Exchange-Native Brackets:** Stop-Loss and Take-Profit orders sit natively in the OKX matching engine. Even if internet or power cuts out, your capital is protected on the exchange.
2. **Dynamic Cross Leverage (3x):** Automated contract multiplier math (`1.0 SOL`, `1000 DOGE`, `0.001 XAU`, `0.01 BTC`, `0.1 ETH`) prevents oversized lot risk.
3. **ISP DNS Poisoning Bypass:** Embedded Cloudflare IPv4 resolution override (`172.64.144.82`) bypasses regional ISP blocks on OKX API domains.
4. **Autonomous Pass-1 Watchdog:** Every 6 seconds, the scanner audits all open positions. Any position missing an active exchange Stop Loss is immediately repaired.

---

## 💬 Support & Inquiries
To request assistance, access, or report an issue:
* Contact **Puzzled Programmer** via official private channels.
