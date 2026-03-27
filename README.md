# ⚠️ This package has moved

This package is now maintained in the [wopr-plugins monorepo](https://github.com/wopr-network/wopr-plugins/tree/main/packages/plugin-browser).

This repository is archived and no longer accepts contributions.

---

# @wopr-network/wopr-plugin-browser

> Browser automation plugin for WOPR — Playwright-based web interaction with persistent session profiles.

## Install

```bash
npm install @wopr-network/wopr-plugin-browser
```

## Usage

```bash
wopr plugin install github:wopr-network/wopr-plugin-browser
```

Then configure via `wopr configure --plugin @wopr-network/wopr-plugin-browser`.

## Configuration

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `headless` | boolean | No | Run browser headlessly (default: `true`) |
| `defaultTimeout` | number | No | Default navigation timeout in ms (default: `30000`) |

## What it does

The browser plugin gives WOPR agents full Playwright-based browser control through A2A tools: `browser_navigate`, `browser_click`, `browser_type`, `browser_screenshot`, and `browser_evaluate`. Browser profiles (cookies, sessions, local storage) persist across invocations via the WOPR Storage API, enabling stateful web automation like filling forms, scraping behind logins, or taking screenshots.

## License

MIT