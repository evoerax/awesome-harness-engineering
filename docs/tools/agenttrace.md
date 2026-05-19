# agenttrace

> Local-first observability for AI coding agent sessions.

## Overview

agenttrace is a TUI and report generator for AI coding agent session history. It reads local logs from multiple coding agents, then surfaces cost, tokens, elapsed time, failures, latency, anomalies, health, diffs, and CI gates.

**GitHub:** https://github.com/luoyuctl/agenttrace
**Site:** https://luoyuctl.github.io/agenttrace/

## Core Idea

Most coding agents leave useful traces on disk, but those traces are scattered across tools and formats. agenttrace normalizes those sessions so teams can inspect slow or expensive runs without uploading private logs to a hosted service.

## Key Features

| Feature | Details |
|---------|---------|
| TUI | Overview, critical sessions, detail, diagnostics, and diff views |
| Reports | JSON, Markdown, and self-contained HTML |
| Health gates | CI checks for average health, critical sessions, and tool failure rate |
| Local-first | Reads local session history and exports only when requested |

## Supported Sources

Claude Code, Codex CLI, Gemini CLI, Qwen Code, Cline, Aider, Cursor exports, Hermes Agent, OpenCode, OpenClaw, Pi, Oh My Pi, Kimi CLI, Copilot-style logs, and generic JSON/JSONL traces.

## Installation

```bash
curl -sL https://raw.githubusercontent.com/luoyuctl/agenttrace/master/install.sh | sh
agenttrace
```

Alternative install paths:

```bash
brew install luoyuctl/tap/agenttrace
go install github.com/luoyuctl/agenttrace/cmd/agenttrace@latest
```

## CI Example

```bash
agenttrace --overview \
  --fail-under-health 80 \
  --fail-on-critical \
  --max-tool-fail-rate 15
```
