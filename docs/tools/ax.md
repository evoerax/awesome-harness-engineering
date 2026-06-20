# ax

> Local telemetry and recall graph for AI coding agents.

## Overview

ax ingests agent transcripts, skills, Git history, and OTLP events into a local
graph. It turns coding-agent work into queries: sessions, costs, tool calls,
skill usage, churn, and workflow recall.

**GitHub:** [Necmttn/ax](https://github.com/Necmttn/ax)

## Core Idea

Coding agents leave traces across many places:

1. transcripts from Claude Code, Codex, Pi, OpenCode, and Cursor,
2. installed skills and agent files,
3. Git commits and project history,
4. OTLP metrics, traces, and logs.

ax normalizes those traces into a local SurrealDB graph and exposes them through
the CLI, dashboard, and read-only MCP server.

## What It Tracks

| Signal | Examples |
| ------ | -------- |
| Sessions | Provider, project, model, started time |
| Turns | User prompts, assistant turns, tool calls |
| Costs | Model, token usage, estimated spend |
| Skills | Installed, loaded, invoked, role-tagged |
| Tools | Tool-call history, verification churn |
| Telemetry | OTLP metrics, spans, Codex log events |
| Git | Commits, repo scope, nearby sessions |

## Unique Feature

**Local graph over agent work** — instead of relying on one harness UI, ax
connects transcripts, costs, skills, tools, OTLP events, and Git history across
harnesses.

## Platform Support

| Platform | Transcript Ingest | OTLP | MCP Queries |
| -------- | :---------------: | :--: | :---------: |
| Claude Code | ✅ | ✅ | ✅ |
| Codex | ✅ | ✅ | ✅ |
| OpenCode | ✅ | ❌ | ✅ |
| Cursor | ✅ | ❌ | ✅ |
| Pi | ✅ | ❌ | ✅ |

## Interfaces

| Interface | Use |
| --------- | --- |
| CLI | `ax sessions`, `ax cost`, `ax skills`, `ax recall` |
| Dashboard | Local studio served by `ax serve` |
| MCP | 18 read-only query tools via `ax mcp` |
| Hooks SDK | Typed hooks for Claude Code and Codex |

## Installation

```bash
curl -fsSL ax.necmttn.com/install | sh
ax install
ax ingest
ax serve
```

Run the MCP server:

```bash
ax mcp
```
