# Blackberrylabs

**BrambleRS shows what AI coding agents do to a Linux machine, most serious first, on one screen. Read-only.**

One program, six modules, one install. BrambleRS reads the configuration, instruction files, transcripts and caches the agents already leave, merges their findings, and writes only its own settings and saved reports.

[Install BrambleRS](https://github.com/blackberrylabs/BrambleRS/releases) with the `.deb`, `.rpm` or AppImage for x86_64 Linux.

## The six modules

| Module | Question |
|---|---|
| **Agent permissions** | What each AI assistant may do without asking, and which setting says so |
| **MCP servers** | Which MCP servers are declared, once per server, with duplicates, clear secrets and dead commands |
| **Instruction files** | Which instruction files each host would load, in which order, and what it would drop |
| **Disk cleanup** | What AI tooling left on the disk, and what could go |
| **Keys & spend** | Which accounts and keys this machine holds, and how many tokens each host burned |
| **Activity** | What the agents actually ran, created, edited or deleted, session by session |

## The promises

- **Read-only.** The only writes are its own settings under `~/.config/bramblers/`, the saved reports and the cleanup script the Disk cleanup tab offers to save under `~/.local/state/bramblers/`.
- **No network of its own.** Nothing is sent anywhere; a link opens in your browser only when you click it.
- **Secrets masked** the moment they are read.
- **Actions shown, never run.** Each finding says what you could do; you do it.
- **Every rule sourced.** The documentation sentence, the source line, or the observation behind each claim is in the module.

## Under the hood

One Rust workspace, MIT: `bramblers-core`, `bramblers-report`, `bramblers-hostrules`, `bramblers-ui`, the iced app, six module cores and their six screens. The source is [blackberrylabs/BrambleRS](https://github.com/blackberrylabs/BrambleRS).

The old tower, the six module repositories, the three foundation crates and the template were
removed on 2026-11-07. BrambleRS is the only source and the only download.

By [Alexandre Do](https://github.com/Nimeria2026). Issues and rules are welcome in the BrambleRS repository.
