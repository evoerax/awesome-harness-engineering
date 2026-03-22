# Gemini CLI

> Google's AI coding agent CLI.

## Overview

Gemini CLI uses an extension system with `GEMINI.md` for context injection. Extensions are installed via `gemini extensions install`.

## Key Features

| Feature | Details |
|---------|---------|
| **Hooks** | ❌ |
| **Extensions** | `gemini extensions install` |
| **Context** | `GEMINI.md` (with `@./path` references) |
| **Config** | `~/.gemini/` |

## Installation

```bash
gemini extensions install https://github.com/obra/superpowers
gemini extensions update superpowers
```

## Tools That Support Gemini CLI

- ✅ Superpowers
- ✅ PUA
- ✅ Get Shit Done
- ✅ gstack

## Links

- [Gemini CLI GitHub](https://github.com/google-gemini/gemini-cli)
