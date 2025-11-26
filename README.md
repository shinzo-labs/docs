<a id="readme-top"></a>
<div align="center">
    <a href="https://github.com/shinzo-labs/docs"><img src="https://github.com/user-attachments/assets/64f5e0ae-6924-41b1-b1da-1b22627e5c43" alt="Logo" width="256" height="256"></a>
    <h1 align="center">
        Shinzo Platform Documentation
    </h1>
    <p align=center>
        <a href="https://github.com/shinzo-labs/docs/stargazers"><img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.github.com%2Frepos%2Fshinzo-labs%2Fdocs%2Fstargazers&query=%24.length&logo=github&label=stars&color=e3b341" alt="Stars"></a>
        <a href="https://github.com/shinzo-labs/docs/forks"><img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.github.com%2Frepos%2Fshinzo-labs%2Fdocs%2Fforks&query=%24.length&logo=github&label=forks&color=8957e5" alt="Forks"></a>
        <a href="https://github.com/shinzo-labs/docs/pulls"><img src="https://img.shields.io/badge/build-passing-green" alt="Build"></a>
        <a href="https://github.com/shinzo-labs/docs/graphs/contributors"><img src="https://img.shields.io/badge/contributors-welcome-339933?logo=github" alt="contributors welcome"></a>
        <a href="https://discord.gg/UYUdSdp5N8"><img src="https://discord-live-members-count-badge.vercel.app/api/discord-members?guildId=1079318797590216784" alt="Discord"></a>
    </p>
    <div align="center">
    </div>
    Welcome to the Shinzo Platform documentation repository. This documentation is built with [Mintlify](https://mintlify.com) and covers our OpenTelemetry-compatible observability platform designed specifically for Model Context Protocol (MCP) developers.
    <p align=center>
        <a href="https://docs.shinzo.ai/"><strong>Explore the docs »</strong></a>
    </p>
</div>

<details>
  <summary>📋 Table of Contents</summary>

  - [🤖 About Shinzo](#about-shinzo)
    - [🏗️ System Architecture](#system-architecture)
    - [✨ Key Features](#key-features)
  - [⚙️ Setup](#setup)
  - [🗺️ Roadmap](#roadmap)
  - [🤝 Contributing](#contributing)
  - [📄 License](#license)
  - [📞 Contact](#contact)
  - [📚 Additional Resources](##additional-resources)
</details>

## What is Shinzo Platform?

Shinzo Platform provides comprehensive observability for MCP servers, offering:

- **MCP-Native Observability**: Purpose-built monitoring for MCP tools, resources, and prompts
- **OpenTelemetry Compatibility**: Industry-standard telemetry with MCP-specific insights
- **Zero-Configuration Instrumentation**: Get started in minutes with our SDKs
- **Privacy-First Design**: Built-in PII sanitization and configurable data processing

## Documentation Structure

The documentation is organized into the following sections:

### Getting Started
- **[Quick Start Guide](/quickstart)** - Get your MCP server instrumented in under 5 minutes

### Concepts
- **[Model Context Protocol (MCP)](/concepts/mcp)** - Understanding MCP and why observability matters for MCP developers
- **[OpenTelemetry](/concepts/opentelemetry)** - How Shinzo leverages OpenTelemetry standards

### Platform
- **[Dashboard](/platform/dashboard)** - Guide to using the Shinzo Platform web dashboard

### SDK Documentation

#### TypeScript SDK
- **[Installation](/sdk/typescript/installation)** - Installing and setting up the TypeScript SDK
- **[Configuration](/sdk/typescript/configuration)** - Advanced configuration options for TypeScript

#### Python SDK
- **[Installation](/sdk/python/installation)** - Installing and setting up the Python SDK
- **[Configuration](/sdk/python/configuration)** - Advanced configuration options for Python

## Local Development

### Prerequisites
- Node.js version 19 or higher
- npm, pnpm, or yarn

### Setup

Install the Mintlify CLI globally:

```bash
npm i -g mint
```

### Running Locally

Navigate to the docs directory and start the development server:

```bash
mint dev
```

Your local preview will be available at `http://localhost:3000`.

### Custom Ports

To run Mintlify on a specific port:

```bash
mint dev --port 3333
```

If a port is already in use, Mintlify will automatically use the next available port.

### Validating Links

Check for broken links in the documentation:

```bash
mint broken-links
```

### Keeping CLI Updated

Update to the latest Mintlify CLI version:

```bash
npm i -g mint@latest
```

## Contributing

We welcome contributions to improve the Shinzo Platform documentation! Here's how you can help:

### Reporting Issues

If you find errors, broken links, or unclear explanations:

1. Check [existing issues](https://github.com/shinzo-labs/docs/issues) to avoid duplicates
2. Open a new issue with a clear description of the problem
3. Include the page URL and suggested improvements

### Submitting Changes

1. **Fork the repository** and create a new branch for your changes
2. **Make your edits** following our writing standards (see below)
3. **Test locally** using `mint dev` to preview your changes
4. **Validate** that all links work using `mint broken-links`
5. **Submit a pull request** with a clear description of your changes

### Writing Standards

When contributing documentation:

- **Voice**: Use passive voice for direct, clear instructions (avoid "you" and "your")
- **Prerequisites**: List prerequisites at the start of procedural content
- **Code examples**: Test all code examples before submitting
- **Formatting**: Match the style and formatting of existing pages
- **Language tags**: Include language tags on all code blocks
- **Alt text**: Add descriptive alt text to all images
- **Links**: Use relative paths for internal links (e.g., `/quickstart` not `https://docs.shinzo.ai/quickstart`)

### Frontmatter Requirements

Every MDX file must include frontmatter with:

```yaml
---
title: "Clear, descriptive page title"
description: "Concise summary for SEO and navigation"
---
```

### Content Strategy

- Document just enough for user success - avoid over-explaining
- Prioritize accuracy and usability
- Make content evergreen when possible
- Search for existing information before adding new content
- Check existing patterns for consistency
- Start by making the smallest reasonable changes

## Publishing Changes

Changes to the documentation are automatically deployed to production when merged to the `main` branch through our GitHub integration.

## Troubleshooting

### Development Server Issues

**Error: Could not load the "sharp" module**
- This may indicate an outdated Node.js version
- Remove the CLI: `npm remove -g mint`
- Upgrade to Node v19 or higher
- Reinstall: `npm i -g mint`

**Unknown errors**
- Delete the `~/.mintlify` folder from your home directory
- Run `mint dev` again

### Links Not Working

Make sure you're using relative paths for internal links:

- ✅ Good: `/quickstart`
- ❌ Bad: `https://docs.shinzo.ai/quickstart`

## Resources

- [Mintlify Documentation](https://mintlify.com/docs)
- [Shinzo Platform](https://app.shinzo.ai)
- [GitHub Repository](https://github.com/shinzo-labs)
- [Support](mailto:austin@shinzolabs.com)

## License

This documentation is maintained by Shinzo Labs under the MIT License.
