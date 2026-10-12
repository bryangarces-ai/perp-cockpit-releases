# Zenthea Perpetuals Cockpit v1.0.0

Autonomous Perpetual Futures Execution Engine & Real-Time Cyberpunk Terminal for OKX Futures.

### 🌟 Key Features
- **Unified Single-Port Cockpit (`http://localhost:8890`):** Full Angular 19+ Cyberpunk UI bundled directly into the standalone binary. Zero external runtime dependencies (no Node.js or Python required on the client PC).
- **The 6-Gate Tactical Strike Radar:** Evaluates Signal Setup (RSI), Volume Fuel (Med20), Regime Guard (ADX), S/R Runway (Donchian), JEV AI Conviction, and Margin Concurrency concurrently.
- **Native OKX OCO Algo Orders:** True exchange-level `ordType: "oco"` bracket execution for immediate, slippage-protected stops and targets.
- **Ironclad Stop-Loss Placement Guarantee ("Never Hold Naked" Policy):** 3-attempt exponential backoff placement, matching engine confirmation (`verify_sl_active`), and fail-safe emergency market close if exchange stops fail.
- **Dynamic Break-Even Management:** Automatically locks Stop Loss at entry + fees once profit reaches 1.0x risk distance.
- **Dual-Environment Architecture:** Seamless switching between OKX Simulated Trading (~$5,100 USDT) and OKX Production API (~$277.32 USDT) with mandatory auto-disarm safety interlocks.
- **Multi-Asset Multiplier Engine:** Precision lot conversions across `SOL` (1.0), `DOGE` (1000.0), `XAU` (0.001), `BTC` (0.01), and `ETH` (0.1).

### 📦 Packages Included
- `ZentheaPerp-v1.0.0-Windows.zip`: Full release package with executable, configuration templates, launcher, and getting started guide.
- `ZentheaPerpCockpit.exe`: Standalone binary for drop-in updates.
