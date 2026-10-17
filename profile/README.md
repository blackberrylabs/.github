# Blackberrylabs

**Everything your AI agents do to your machine, on one screen. Read-only, like the tools behind it.**

Small desktop tools for developers and vibe coders who run AI on Linux. Each one answers one question about your machine, shows its evidence, and never acts in your place — you read, you decide, you act with the host's own settings or a script you have read. The control tower gathers them.

## Start here: the control tower

**[Blackberrylabs](https://github.com/blackberrylabs/blackberrylabs)** — one screen that says what is wrong on your machine on the AI side, most serious first — *act now · review · good to know · information* — and opens the right tool at the right place. Install it, then whichever modules you want; it works with any subset and shows the others as available.

[Get it](https://github.com/blackberrylabs/blackberrylabs/releases) — `.deb`, `.rpm`, AppImage.

## The modules

| | Verb | What it answers |
|---|---|---|
| **[Permitt](https://github.com/blackberrylabs/permitt)** | inspect | What each AI assistant may do without asking — run commands, edit files, reach the network, call MCP tools — and which setting, in which file, says so. 16 hosts. Shell start-up files checked for bypass flags. |
| **[MCProster](https://github.com/blackberrylabs/mcproster)** | inventory | Every MCP server declared on the machine, once, with the hosts and files that declare it — duplicates, secrets in clear, missing commands, skipped confirmations, what each server costs in the model's context. |
| **[Cleanator](https://github.com/blackberrylabs/cleanator)** | clean | What AI tooling left on the disk — model stores, caches, build outputs, abandoned environments — and what could go, as a script you read and run yourself. Never deletes anything. |
| **[Linstruct](https://github.com/blackberrylabs/linstruct)** | lint | Your AI instruction files — CLAUDE.md, AGENTS.md, .cursor/rules, copilot instructions, GEMINI.md… — as each agent will actually read them: what it cuts past its budget, what it never reads, what another file shadows, what costs context twice. 19 hosts, every rule sourced. |

## The promises, the same for every tool

- **Read-only.** No file is written outside the tool's own preferences (and, for the tower, its saved reports).
- **No network.** Nothing leaves the machine; links are shown, never followed.
- **Secrets masked** the moment they are read.
- **Actions shown, never run.** Each finding says what you could do; you do it.
- **Every rule sourced.** The documentation sentence, the source line, or the observation behind each claim is in the tool.

## Under the hood

Three shared crates, all Rust, all MIT: **[bbl-hostrules](https://github.com/blackberrylabs/bbl-hostrules)** (where each AI assistant keeps its files, how to read them without writing), **[bbl-ui](https://github.com/blackberrylabs/bbl-ui)** (the shared face), **[bbl-report](https://github.com/blackberrylabs/bbl-report)** (the contract between the tower and its modules). Adding a module to the family = a binary that answers `report` and one declarative sheet in the tower.

By [Alexandre Do](https://github.com/Nimeria2026). Issues and rules welcome in each repository.
