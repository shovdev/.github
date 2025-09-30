<!-- Note: This file is automatically synced from the private /shov monorepo. -->
<!-- Triggering sync -->

<div align="center">
  <img src="https://shov.com/logos/shov-logo-white.svg" alt="Shov Logo" width="150"/>
</div>

<h1 align="center">Instant backends for AI-coded apps</h1>

<p align="center">
  <strong>Instant, serverless memory infrastructure for AI applications and prototypes.</strong>
  <br />
  Every record you store is instantly vector-searchable. No setup, no extra services.
</p>

<p align="center">
  <a href="https://shov.com" target="_blank"><strong>Website / Docs</strong></a> •
  <a href="https://github.com/shovdev" target="_blank"><img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white" alt="GitHub"></a> •
  <a href="https://x.com/shovdev" target="_blank"><img src="https://img.shields.io/badge/X-000000?style=flat&logo=x&logoColor=white" alt="X"></a> •
  <a href="https://www.reddit.com/r/shov/" target="_blank"><img src="https://img.shields.io/badge/Reddit-FF4500?style=flat&logo=reddit&logoColor=white" alt="Reddit"></a> •
  <a href="https://discord.gg/GB3rDcFrGz" target="_blank"><img src="https://img.shields.io/badge/Discord-5865F2?style=flat&logo=discord&logoColor=white" alt="Discord"></a>
</p>

---

## What is Shov?

Shov is a serverless data layer built on Cloudflare's global network, designed to eliminate all setup friction for developers building modern applications. It provides five core data primitives with zero configuration:

-   **Key/Value Store:** For configuration, sessions, and simple data.
-   **JSON Collections:** For structured objects like users, products, or logs.
-   **File Storage:** For any file type, delivered globally via CDN.
-   **Vector Search:** For powerful semantic search across all your data.
-   **Real-time Streaming:** For live updates, chat, and collaborative features.

Every piece of data you write to the Key/Value store or a Collection is **automatically embedded and indexed** for vector search, giving your application an AI-native memory out of the box.

## Blazing Fast Performance

Shov is built on Cloudflare's global network to deliver consistent, low-latency performance wherever your users are.

| Metric               | Typical Latency | Description                           |
| -------------------- | --------------- | ------------------------------------- |
| **Cached Reads**     | `~0.03ms`       | Write-through cached reads at edge.   |
| **Cold Reads**       | `~80ms`         | Uncached reads from origin.           |
| **Batch Operations** | `~19ms`         | Atomic batch operations per item.     |

## Quick Start: Zero to AI Memory in 30 Seconds

You don't need an account or credit card to get started.

### 1. Install the CLI
```bash
npm install -g shov
```

### 2. Create Your Project
This single command provisions a new project on Cloudflare's global network, instantly giving you a database, file storage, a vector index, and a secure API key. No sign-up required.

```bash
shov new my-first-project
#
# ✔ Project 'my-first-project' created
# ✔ API Key: shov_live_...
#
```

### 3. Start Building
Your backend is ready. Use your new API key with the CLI or SDKs to start building.

**Example A: Simple Key/Value**
```bash
# Set a value at the edge
shov set greeting "Hello from Shov"

# Get it back instantly from anywhere
shov get greeting
# > "Hello from Shov"
```

**Example B: AI-Powered Collections**
```bash
# Add a collection of items
shov add-many products '[
  { "name": "Fender Stratocaster", "type": "Electric Guitar" },
  { "name": "Ibanez RG550", "type": "Electric Guitar" },
  { "name": "Roland TD-27KV", "type": "Electronic Drums" }
]'

# Find them with semantic search
shov search "a stringed instrument" -c products
# > [
# >   { "name": "Fender Stratocaster", "type": "Electric Guitar" },
# >   { "name": "Ibanez RG550", "type": "Electric Guitar" }
# > ]

# Advanced search with filters and JSON output
shov search "musical equipment" --filters '{"type": "Electric Guitar"}' --json

# See all items in your project
shov contents

# Clear a collection
shov clear products
```

**Example C: Real-time Streaming**
```bash
# Subscribe to real-time updates (in one terminal)
shov subscribe '[{"collection": "users"}, {"key": "config"}]'
# > ✅ Connected to stream!
# > 📡 Listening for real-time updates...

# In another terminal, make changes to see live updates
shov add users '{"name": "Alice", "status": "active"}'
shov set config '{"theme": "dark"}'

# Broadcast custom messages to subscribers
shov broadcast '{"channel": "notifications"}' '{"text": "System maintenance in 5 minutes"}'
```

That's it. You now have a fully-featured, globally-replicated backend with AI search capabilities and real-time streaming.

## Our Public Packages

This organization is home to the clients and tools for interacting with the Shov platform.

### SDKs

| Language       | Package                                     | Repository                                       |
| -------------- | ------------------------------------------- | ------------------------------------------------ |
| **JavaScript** | [`shov-js`](https://www.npmjs.com/package/shov-js) | [shov-js](./shov-js)                     |

### Command Line Interface (CLI)

| Package                               | Repository                             |
| ------------------------------------- | -------------------------------------- |
| [`shov`](https://www.npmjs.com/package/shov) | [shov-cli](./shov-cli)                 |


## Contributing

We welcome community contributions to our public packages and tools. 


---

<p align="center">
  <a href="https://shov.com/login" target="_blank">Get Started for Free</a>
</p>
