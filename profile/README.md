<!-- Note: This file is automatically synced from the private /shov monorepo. -->
<!-- Triggering sync -->

<div align="center">
  <img src="https://raw.githubusercontent.com/shov-com/shov/master/public/logos/shov-logo-white.svg" alt="Shov Logo" width="400"/>
</div>

<h1 align="center">The AI Memory Engine</h1>

<p align="center">
  <strong>Instant, serverless infrastructure for AI applications and prototypes.</strong>
  <br />
  Every record you store is instantly vector-searchable. No setup, no extra services.
</p>

<p align="center">
  <a href="https://shov.com"><strong>Website</strong></a> ·
  <a href="https://shov.com/docs"><strong>Documentation</strong></a> ·
  <a href="https://shov.com/blog"><strong>Blog</strong></a>
</p>

---

## What is Shov?

Shov is a serverless data layer built on Cloudflare's global network, designed to eliminate all setup friction for developers building modern applications. It provides four core data primitives with zero configuration:

-   **Key/Value Store:** For configuration, sessions, and simple data.
-   **JSON Collections:** For structured objects like users, products, or logs.
-   **File Storage:** For any file type, delivered globally via CDN.
-   **Vector Search:** For powerful semantic search across all your data.

Every piece of data you write to the Key/Value store or a Collection is **automatically embedded and indexed** for vector search, giving your application an AI-native memory out of the box.

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

We are building Shov in the open and welcome community contributions. Please see our main [Contributing Guide](https://github.com/shov-com/.github/blob/main/CONTRIBUTING.md) and [Code of Conduct](https://github.com/shov-com/.github/blob/main/CODE_OF_CONDUCT.md) for more information.

---

<p align="center">
  <a href="https://shov.com/login">Get Started for Free</a>
</p>
