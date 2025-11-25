# claudeops

> Forked from [ccflare](https://github.com/snipeship/ccflare) by [snipeship](https://github.com/snipeship)

**Track Every Request. Go Low-Level. Never Hit Rate Limits Again.**

The ultimate Claude API proxy with intelligent load balancing across multiple accounts. Full visibility into every request, response, and rate limit.

https://github.com/user-attachments/assets/c859872f-ca5e-4f8b-b6a0-7cc7461fe62a

![claudeops Dashboard](apps/lander/src/screenshot-dashboard.png)

## Why claudeops?

- **Zero Rate Limit Errors** - Automatically distribute requests across multiple accounts
- **Request-Level Analytics** - Track latency, token usage, and costs in real-time
- **Deep Debugging** - Full request/response logging and error traces
- **<10ms Overhead** - Minimal performance impact on your API calls
- **Free & Open Source** - Run it yourself, modify it, own your infrastructure

## Quick Start

```bash
# Clone and install
git clone https://github.com/frankekn/claudeops
cd claudeops
bun install

# Start claudeops (TUI + Server)
bun run claudeops

# Configure Claude SDK
export ANTHROPIC_BASE_URL=http://localhost:8080
```

## Features

### Intelligent Load Balancing
- **Session-based** - Maintain conversation context (5hr sessions)

### Real-Time Analytics
- Token usage tracking per request
- Response time monitoring
- Rate limit detection and warnings
- Cost estimation and budgeting

### Developer Tools
- Interactive TUI (`bun run claudeops`)
- Web dashboard (`http://localhost:8080/dashboard`)
- CLI for account management
- REST API for automation

### Production Ready
- Automatic failover between accounts
- OAuth token refresh handling
- SQLite database for persistence
- Configurable retry logic

## Documentation

Full documentation available in [`docs/`](docs/):
- [Getting Started](docs/index.md)
- [Architecture](docs/architecture.md)
- [API Reference](docs/api-http.md)
- [Configuration](docs/configuration.md)
- [Load Balancing Strategies](docs/load-balancing.md)

## Screenshots

<table>
  <tr>
    <td><img src="apps/lander/src/screenshot-dashboard.png" alt="Dashboard"/></td>
    <td><img src="apps/lander/src/screenshot-logs.png" alt="Logs"/></td>
  </tr>
  <tr>
    <td align="center"><b>Real-time Dashboard</b></td>
    <td align="center"><b>Request Logs</b></td>
  </tr>
  <tr>
    <td colspan="2"><img src="apps/lander/src/screenshot-analytics.png" alt="Analytics"/></td>
  </tr>
  <tr>
    <td colspan="2" align="center"><b>Analytics & Usage Tracking</b></td>
  </tr>
</table>

## Requirements

- [Bun](https://bun.sh) >= 1.2.8
- Claude API accounts (Free, Pro, or Team)

## Contributing

We welcome contributions! See [CONTRIBUTING.md](docs/contributing.md) for guidelines.

## License

MIT - See [LICENSE](LICENSE) for details

---

<p align="center">
  Built for developers who ship
</p>

[![Mentioned in Awesome Claude Code](https://awesome.re/mentioned-badge-flat.svg)](https://github.com/hesreallyhim/awesome-claude-code)
