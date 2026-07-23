# James Maes

Startup and Growth CTO. Software Engineer at heart.
Founder at [QRun-IO](https://github.com/QRun-IO). Full-time CTO at [Me.Health](https://www.me.health).
Currently building GFS.

Twenty-plus years building teams, companies, and the software they run on.
Most of the work isn't on GitHub.

---

### Work

**At QRun-IO**

**[QQQ](https://github.com/QRun-IO/qqq)** &nbsp;—&nbsp; Metadata-driven application framework for Java. Define your data model and business rules through metadata, and QQQ generates the working application — REST API, React dashboard, CLI, and Lambda handlers from the same codebase. Apache 2.0, stable, used in production.

**[qqq-business-platform](https://github.com/QRun-IO/qqq-business-platform)** &nbsp;—&nbsp; Complete self-hosted business platform (CMS, newsletter, auth, admin dashboard) built on QQQ. A production-ready open-source alternative to Squarespace, ConvertKit, and HubSpot.

The surrounding ecosystem includes [qctl](https://github.com/QRun-IO/qctl) (CLI), [qqq-frontend-material-dashboard](https://github.com/QRun-IO/qqq-frontend-material-dashboard) (React admin UI), [qbit-middleware-mcp](https://github.com/QRun-IO/qbit-middleware-mcp) (MCP middleware exposing QQQ backends as AI agent tools), [qqq-android](https://github.com/QRun-IO/qqq-android), and a growing library of [QBits](https://github.com/orgs/QRun-IO/repositories?q=qbit) covering CRM, WMS, workflows, webhooks, and RBAC.

**Sovereign Systems & Messaging**

**[Nuncio](https://github.com/KofTwentyTwo/nuncio)** &nbsp;—&nbsp; *nūntiō: I announce, I deliver a message.* Sovereign Mail, Calendar & Contacts Suite with 100% multi-shell parity across Desktop GUI (Tauri v2 + React 18), Terminal TUI (Ratatui), POSIX CLI (`nuncio-cli`), and Native MCP AI Server (`nuncio-mcp`). Driven by a central background daemon (`nunciod`) with SQLite WAL, FTS5 trigram search, and local Age/OS Keyring encryption. [nuncio.mx](https://nuncio.mx)

**[Concilium](https://github.com/KofTwentyTwo/Concilium)** &nbsp;—&nbsp; Master-agent orchestration platform for multi-repository software delivery. A *Master Project* groups multiple repos into one logical system; a persistent *Master Agent* decomposes initiatives and coordinates per-repo agents — each deeply familiar with its codebase — to plan, execute, and converge work across the whole stack. Java 21 + QQQ + PostgreSQL backend with a Next.js command center.

**Infrastructure & Governance**

**[Praetor](https://github.com/KofTwentyTwo/Praetor)** &nbsp;—&nbsp; *to lead, to command.* Centralized infrastructure-as-code repository for the Galaxy LAN. OpenTofu provisions Talos Linux Kubernetes clusters on Proxmox; Helm charts handle full bootstrap (Traefik, cert-manager, ArgoCD, Prometheus, kube-vip, metrics-server); UniFi Controller API automation handles local DNS.

**[Munitor](https://github.com/KofTwentyTwo/Munitor)** &nbsp;—&nbsp; *fortifier; one who builds defenses.* Unified CircleCI orb for building, testing, and deploying every repo across the organization. Dynamic configuration generates runtime pipelines (Node APIs, Java webapps, Docker GHCR push, SBOM, SAST, GitOps CD, GitFlow enforcement) from a single `.munitor.yml` manifest.

**[Nix Dotfiles](https://github.com/KofTwentyTwo/nix)** &nbsp;—&nbsp; Personal declarative system and home-manager flake maintaining reproducible developer environments across a multi-macOS Apple Silicon fleet. Manages toolchains, shell configuration, Neovim plugins, AI agent rules, and secret deployment.

**Local-First AI & Vision**

**[Jarvis](https://github.com/KofTwentyTwo/Jarvis)** &nbsp;—&nbsp; Always-on macOS AI assistant in the shape of the Iron Man HUD. A Swift host owns the OS surface (mic, camera, hotkeys, persistent storage) and the agent loop streaming Claude Opus 4.7 with Ollama as a first-class local fallback; a `WKWebView` mounts a React + React Three Fiber HUD as a pure rendering surface. Tools ride MCP; voice and vector memory stay 100% local.

**[MetalPOC](https://github.com/KofTwentyTwo/MetalPOC)** &nbsp;—&nbsp; Transparent HUD drawn entirely in Apple Metal: central animated orb + 10 dynamic widgets floating click-through on every desktop Space with CoreText rasterization and sub-pixel marquee scrolling.

**[VoicePOC](https://github.com/KofTwentyTwo/VoicePOC)** &nbsp;—&nbsp; Local-first macOS voice loop using WhisperKit for STT, Ollama for LLM, and AVSpeech for TTS with zero cloud round-trips.

**[VisionPOC](https://github.com/KofTwentyTwo/VisionPOC)** &nbsp;—&nbsp; Camera + Apple Neural Engine + Metal proving ground running live video through GPU/ANE into synchronized views with YOLOv8x detection across 601 classes, pose skeletons, and 60 Hz tracked motion smoothing.

**Developer Tooling & CLIs**

**[gclo](https://github.com/KofTwentyTwo/gclo)** / **[gclo-macos](https://github.com/KofTwentyTwo/gclo-macos)** &nbsp;—&nbsp; Git Clone Large Organizations. Desktop GUI and CLI tools (Windows 11 in Go/C# and native macOS in Swift 6/AppKit) that clone and sync every repository across a GitHub organization in parallel.

**[notion-sql](https://github.com/KofTwentyTwo/notion-sql)** &nbsp;—&nbsp; SQL interface for Notion databases. A Rust CLI that parses SQL with `sqlparser`, introspects Notion database schemas, and translates CRUD statements into typed Notion API calls.

**[limen](https://github.com/KofTwentyTwo/limen)** &nbsp;—&nbsp; *threshold.* Two-stage terminal launcher TUI in Go + Bubble Tea that runs before tmux to select hosts, check reachability, and manage sessions with zero deliberation tax.

**[Claritas](https://github.com/KofTwentyTwo/Claritas)** &nbsp;—&nbsp; Code-style intelligence plugin for IntelliJ. PSI-based Kotlin core enforcing team comment formatting, Javadoc generation, and flower-boxing across codebases.

**[obsidian-penny](https://github.com/KofTwentyTwo/obsidian-penny)** &nbsp;—&nbsp; PENNY — Prose Engine for Narrative, Notes, and Yarns. AI co-authoring plugin for Obsidian routing passage rewrites by task complexity across Anthropic API and Ollama models.

**[license-tool](https://github.com/KofTwentyTwo/license-tool)** &nbsp;—&nbsp; CLI utility to audit, validate, and standardize open-source license headers and metadata across multi-repository organizations.

---

### Install

Public CLIs are published as Homebrew formulas — install with one line, update with `brew upgrade`.

```sh
# notion-sql — SQL interface for Notion databases (Rust CLI)
brew install KofTwentyTwo/tap/notion-sql

# limen — terminal launcher TUI for tmux + ssh
brew install KofTwentyTwo/tap/limen

# qctl — CLI for the QRun-IO / QQQ ecosystem
brew install QRun-IO/qctl/qctl
```

Taps: [KofTwentyTwo/tap](https://github.com/KofTwentyTwo/homebrew-tap) · [QRun-IO/qctl](https://github.com/QRun-IO/homebrew-qctl)

---

### Writing & Projects

Longer-form essays and project notes live at [kof22.com](https://www.kof22.com):

- **[Blogs](https://www.kof22.com/blogs)** &nbsp;—&nbsp; essays, notes, and the occasional opinion.
- **[Projects](https://www.kof22.com/projects)** &nbsp;—&nbsp; the work behind what's in this README, in longer form.

---

St. Louis &nbsp;·&nbsp; [kof22.com](https://www.kof22.com) &nbsp;·&nbsp; [LinkedIn](https://linkedin.com/in/james-maes) &nbsp;·&nbsp; [Mastodon](https://mastodon.social/@koftwentytwo)
