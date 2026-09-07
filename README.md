# 📈 QuantPulse • Financial Charting & Market Analytics Terminal

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![TradingView](https://img.shields.io/badge/TradingView-Integration-1E53E5?logo=tradingview&logoColor=white)](https://www.tradingview.com/)
[![Node.js](https://img.shields.io/badge/Node.js-20.x-339933?logo=nodedotjs&logoColor=white)](https://nodejs.org/)

> **QuantPulse** is a modern, web-based financial charting dashboard and technical analysis terminal designed for real-time market data visualization, custom algorithmic studies, and multi-asset tracking.

---

## 🚀 Key Features

* 📊 **High-Performance Canvas Charts:** Ultra-responsive multi-timeframe candlestick and line charts with custom drawing tools.
* ⚡ **Real-Time Market Data Feeds:** Built-in WebSocket adapters supporting Binance, Coinbase, and Kraken ticker streams.
* 🧮 **Technical Analysis & Study Engine:** Core library for moving averages (SMA/EMA/HMA), volatility bands (Bollinger, ATR), momentum oscillators (RSI, MACD), and volume profiles.
* 🎨 **Clean Financial UI:** Dark/light modular themes, responsive grid layout, and customizable workspaces.
* 🔌 **Extensible API:** Easily connect custom backend market data feeds via standard UDF (Universal Data Feed) or REST/WebSocket protocols.

---

## 🏗️ Architecture Overview

```
┌─────────────────────────────────────────────────────────────┐
│                   QuantPulse Web Client                     │
├──────────────────────────────┬──────────────────────────────┤
│      Market UI & Panels      │     Chart & Overlay Engine   │
├──────────────────────────────┼──────────────────────────────┤
│ • Watchlists & Order Books   │ • Canvas Chart Rendering     │
│ • Real-time Ticker Bar       │ • Custom Technical Studies   │
│ • Timeframe & Symbol Picker  │ • Volume & Momentum Panels   │
└──────────────────────────────┴──────────────────────────────┘
                               │
               ┌───────────────┴───────────────┐
               ▼                               ▼
       WebSocket Live Feeds             REST Datafeed (UDF)
   (Binance / Coinbase / Custom)     (Historical Candlesticks)
```

---

## 🛠️ Technology Stack

* **Frontend:** React / TypeScript, HTML5 Canvas, TailwindCSS / Modern CSS Modules
* **Charting Engine:** TradingView Charting Library / Canvas Engine
* **Networking:** WebSockets, Fetch API, UDF Datafeed Protocol
* **Build System:** Vite / Rollup

---

## 📦 Getting Started

### 1. Clone & Install

```bash
# Clone the repository
git clone https://github.com/KITTclick/indicator-app.git

# Navigate to directory
cd indicator-app

# Install dependencies
npm install
```

### 2. Run Locally

```bash
# Start local development server
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser to view the terminal.

---

## ⚙️ Configuration & Data Feeds

Configure your custom data feed endpoint in `src/config/datafeed.ts`:

```typescript
export const datafeedConfig = {
  defaultSymbol: 'BTCUSDT',
  defaultInterval: '15m',
  supportedResolutions: ['1', '5', '15', '60', '240', 'D', 'W'],
  websocketEndpoint: 'wss://stream.binance.com:9443/ws',
};
```

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
