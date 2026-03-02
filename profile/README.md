<h1 align="center">
  🔬 SensorCore
</h1>

<p align="center">
  <b>Real-time analytics and logging platform for mobile and web apps.</b><br/>
  Collect logs, analyze user behavior with ML, run A/B tests, and manage Remote Config — all from your ai agent
</p>

<p align="center">
  <a href="https://sensorcore.dev"><b>🌐 sensorcore.dev</b></a> &nbsp;·&nbsp;
  <a href="https://www.npmjs.com/package/sensorcore">npm</a> &nbsp;·&nbsp;
  <a href="https://github.com/sensorcore/ios">Swift Package</a>
</p>

---

## What is SensorCore?

Your AI agent already writes code — let it handle analytics too.
Paywall conversions, event correlations, user errors — all answered in chat. No dashboards needed.

**Core capabilities:**

| Feature | Description |
|---|---|
| 📊 **Logging** | Structured logs with levels, metadata, and user attribution |
| 🔍 **ML Analytics** | Anomaly detection, user clustering, funnel analysis, behavioral cohorts |
| 🧪 **A/B Testing** | Sticky variant assignment with statistical significance testing |
| 🎛️ **Remote Config** | Toggle feature flags instantly without shipping a new build |
| 🤖 **AI Agent Integration** | MCP server lets AI coding agents analyze your data directly |

---

## Repositories

### SDKs

| Repo | Platform | Install |
|---|---|---|
| **[ios](https://github.com/sensorcore/ios)** | Swift · iOS 15+ | `.package(url: "https://github.com/sensorcore/ios", from: "1.1.1")` |
| **[js](https://github.com/sensorcore/js)** | TypeScript · Browser & Node.js 18+ | `npm install sensorcore` |

Both SDKs share the same design philosophy:

- ⚡ **Zero dependencies** — no bloat, no supply chain risk
- 🔥 **Fire-and-forget** — async batching, retry, offline queue built in
- 🛡️ **Rate-limit aware** — automatic circuit breaker if server throttles
- 📦 **Tiny footprint** — under 25 KB gzipped

### AI Agent Skills

| Repo | Description |
|---|---|
| **[skills](https://github.com/sensorcore/skills)** | Teach your AI coding agent (Cursor, Windsurf, Codex, etc.) how to integrate SensorCore logging and analyze production data via MCP |

Install with one command:

```bash
curl -fsSL https://raw.githubusercontent.com/sensorcore/skills/main/install.sh | bash
```

---

## Quick Start

### 1. Create an account

Go to **[sensorcore.dev](https://sensorcore.dev)** and create a free project. You'll get an API key starting with `sc_`.

### 2. Add the SDK

**iOS (Swift)**

```swift
import SensorCoreiOS

SensorCore.configure(apiKey: "sc_YOUR_API_KEY")
SensorCore.log("App Launched")
```

**JavaScript / TypeScript**

```typescript
import SensorCore from 'sensorcore';

SensorCore.configure({ apiKey: 'sc_YOUR_API_KEY' });
SensorCore.log('App Launched');
```

### 3. See your data

Open the SensorCore dashboard — logs appear in real time. Use the built-in ML tools to detect anomalies, analyze funnels, and understand user behavior.

### 4. Connect your AI agent (optional)

Install the [skills pack](https://github.com/sensorcore/skills) and your AI coding agent gains the ability to:

- Add proper logging to your codebase
- Query your production data via natural language
- Detect conversion issues and suggest fixes
- Manage Remote Config flags

---

## Architecture Overview

```
┌──────────────┐     ┌─────────────┐     ┌──────────────────┐
│  iOS App     │     │  Web App    │     │  AI Agent        │
│  (Swift SDK) │     │  (JS SDK)   │     │  (MCP Skills)    │
└──────┬───────┘     └──────┬──────┘     └────────┬─────────┘
       │                    │                     │
       ▼                    ▼                     ▼
   ┌───────────────────────────────────────────────────┐
   │              api.sensorcore.dev                   │
   │  ┌─────────┐  ┌──────────┐  ┌──────────────────┐  │
   │  │  Logs   │  │ Analytics│  │  Remote Config   │  │
   │  │  API    │  │  ML/MCP  │  │  & A/B Testing   │  │
   │  └─────────┘  └──────────┘  └──────────────────┘  │
   └───────────────────────────────────────────────────┘
```

---

<p align="center">
  Built with ❤️ for developers who ship fast<br/>
  <a href="https://sensorcore.dev"><b>sensorcore.dev</b></a>
</p>
