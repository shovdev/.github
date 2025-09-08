<!-- Note: This file is automatically synced from the private /shov monorepo. -->
<!-- Triggering sync -->

<div align="center">
  <img src="https://shov.com/logos/shov-logo-white.svg" alt="Shov Logo" width="150"/>
</div>

<h1 align="center">The AI Memory Engine</h1>

<p align="center">
  <strong>Instant, serverless memory infrastructure for AI applications and prototypes.</strong>
  <br />
  Every record you store is instantly vector-searchable. No setup, no extra services.
</p>

<p align="center">
  <a href="https://shov.com"><strong>Website / Docs</strong></a>  
</p>

---

## What is Shov?

Shov is a serverless data layer built on Cloudflare's global network, designed to eliminate all setup friction for developers building modern applications. It provides four core data primitives with zero configuration:

-   **Key/Value Store:** For configuration, sessions, and simple data.
-   **JSON Collections:** For structured objects like users, products, or logs.
-   **File Storage:** For any file type, delivered globally via CDN.
-   **Vector Search:** For powerful semantic search across all your data.

Every piece of data you write to the Key/Value store or a Collection is **automatically embedded and indexed** for vector search, giving your application an AI-native memory out of the box.

## Quick Start: Zero to AI Memory in 30 Seconds

You don't need an account or credit card to get started.

### 1. Install the CLI

```bash
npm install -g shov
```

### 2. Create a Project & Add Data

This command provisions a new project and adds a collection of musical instruments.

```bash
shov new my-music-store
shov add-many products '[
  { "name": "Fender Stratocaster", "type": "Electric Guitar" },
  { "name": "Ibanez RG550", "type": "Electric Guitar" },
  { "name": "Roland TD-27KV", "type": "Electronic Drums" }
]'
```

### 3. Search Semantically

Your backend is ready. Use vector search to find instruments by meaning, not just keywords.

```bash
shov search products "a stringed instrument"
# > [
# >   { "name": "Fender Stratocaster", "type": "Electric Guitar" },
# >   { "name": "Ibanez RG550", "type": "Electric Guitar" }
# > ]
```

That's it. You now have a fully-featured, globally-replicated backend with AI search capabilities.

## Blazing Fast Performance

Shov is built on Cloudflare's global network to deliver consistent, low-latency performance wherever your users are.

| Metric          | Typical Latency | Description                  |
| --------------- | --------------- | ---------------------------- |
| **Edge Reads**  | `~50ms`         | Cached reads at the edge.    |
| **Cold Reads**  | `~62ms`         | Uncached reads from origin.  |
| **Edge Writes** | `~55ms`         | Writes replicated globally.  |

## Our Public Packages

This organization is home to the open-source clients and tools for interacting with the Shov platform.

### SDKs

| Language       | Package                                     | Repository                                       |
| -------------- | ------------------------------------------- | ------------------------------------------------ |
| **JavaScript** | [`shov-sdk`](https://www.npmjs.com/package/shov-sdk) | [shov-sdk-js](./shov-sdk-js)                     |
| **Python**     | `(coming soon)`                             | `(coming soon)`                                  |
| **Go**         | `(coming soon)`                             | `(coming soon)`                                  |

### Command Line Interface (CLI)

| Package                               | Repository                             |
| ------------------------------------- | -------------------------------------- |
| [`shov`](https://www.npmjs.com/package/shov) | [shov-cli](./shov-cli)                 |

### Examples

Explore practical, real-world examples of how to build with Shov in our examples repository.

| Description                               | Repository                                   |
| ----------------------------------------- | ------------------------------------------ |
| Sample apps and common use-cases          | [shov-examples](./shov-examples)             |

## Contributing

We are building Shov in the open and welcome community contributions. 

---

<p align="center">
  <a href="https://shov.com/login">Get Started for Free</a>
</p>
