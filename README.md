# James Maes

Startup and Growth CTO. Software Engineer at heart.
Founder at [QRun-IO](https://github.com/QRun-IO). Full-time CTO at [Me.Health](https://www.me.health).
Currently building GFS.

Twenty-plus years building teams, companies, and the software they run on.
Most of the work isn't on GitHub.

---

### Work

**At QRun-IO**

**[QQQ](https://github.com/QRun-IO/qqq)** &nbsp;—&nbsp; Metadata-driven application framework for Java. Define your data model and business rules through metadata, and QQQ generates the working application — REST API, React dashboard, CLI, and Lambda handlers from the same codebase. Not a no-code tool: you write Java for the 20% that's custom and skip the 80% that's the same across every internal tool, admin panel, or CRUD-heavy system. Apache 2.0, stable, used in production.

The framework QRun-IO is built on. Surrounding it: [qctl](https://github.com/QRun-IO/qctl) (CLI), [qqq-frontend-material-dashboard](https://github.com/QRun-IO/qqq-frontend-material-dashboard) (React admin UI), [qqq-android](https://github.com/QRun-IO/qqq-android), and a growing library of [QBits](https://github.com/orgs/QRun-IO/repositories?q=qbit) — drop-in extensions covering CRM, WMS, workflows, webhooks, RBAC, MCP middleware, and more.

**Orchestration & Governance**

**[Concilium](https://github.com/KofTwentyTwo/Concilium)** &nbsp;—&nbsp; Master-agent orchestration platform for multi-repository software delivery. A *Master Project* groups multiple repos into one logical system; a persistent *Master Agent* decomposes initiatives and coordinates per-repo agents — each deeply familiar with its codebase — to plan, execute, and converge work across the whole stack. Planner and coordinator first, not a coding chatbot. Java 21 + QQQ + PostgreSQL backend, Next.js command-center frontend, Claude Code for heavy reasoning with the Claude API for lightweight tasks.

**[Praetor](https://github.com/KofTwentyTwo/Praetor)** &nbsp;—&nbsp; *to lead, to command.* The centralized infrastructure-as-code repository for the Galaxy LAN. OpenTofu provisions Talos Linux Kubernetes clusters on Proxmox; Helm charts handle the full bootstrap (Traefik, cert-manager, ArgoCD, Prometheus, kube-vip, metrics-server); DNS is automated against the UniFi Controller API. Everything version-controlled, peer-reviewable, and `git-crypt`-encrypted where it needs to be.

**[Munitor](https://github.com/KofTwentyTwo/Munitor)** &nbsp;—&nbsp; *fortifier; one who builds defenses.* A unified CircleCI orb for building, testing, and deploying every repo in the org — pipeline changes happen in one place instead of 80+ repos. Each project drops in a minimal `.circleci/config.yml` and a `.munitor.yml` declaring what it needs; Munitor uses CircleCI dynamic configuration to generate the right pipeline at runtime (Node APIs, Java webapps, Docker push, SBOM, SAST, GitOps CD, branch-name GitFlow enforcement, the lot).

**Local-first AI**

**[Jarvis](https://github.com/KofTwentyTwo/Jarvis)** &nbsp;—&nbsp; Always-on macOS AI assistant in the shape of the Iron Man HUD. A Swift host owns the OS surface (mic, camera, hotkeys, persistent storage) and the agent loop streaming Claude Opus 4.7 with Ollama as a first-class local fallback; a `WKWebView` mounts a React + React Three Fiber HUD as a pure rendering surface. Tools ride MCP. Voice (wake-word, STT, TTS) and memory (SQLite + FTS5 + `sqlite-vec` + mem0-style extraction) are fully local — no cloud STT/TTS, no remote embeddings. Eighteen boundary-gate linters keep the Swift↔JS isolation honest. The three POCs below are its rendering, voice, and vision stacks.

**[MetalPOC](https://github.com/KofTwentyTwo/MetalPOC)** &nbsp;—&nbsp; The rendering spine. A Jarvis-style transparent HUD drawn entirely in Apple Metal: a central animated orb surrounded by ten dynamic widgets, floating click-through over your desktop on every Space. Five shader pipelines plus a two-pass glitch post-process, CoreText→MTLTexture text rasterization with sub-pixel marquee scrolling, per-widget `NSVisualEffectView` backdrops clipped to chamfered shapes for the frosted-glass look.

**[VoicePOC](https://github.com/KofTwentyTwo/VoicePOC)** &nbsp;—&nbsp; The voice stack. A standalone local-first conversation loop on macOS — WhisperKit for STT, Ollama for the LLM, AVSpeech for TTS, hotkey-driven, no cloud round-trips.

**[VisionPOC](https://github.com/KofTwentyTwo/VisionPOC)** &nbsp;—&nbsp; The camera + ANE + Metal proving ground. Live video runs through the GPU and Apple Neural Engine into four synchronized views — LIVE, JARVIS-stylized, EDGES (Sobel), and ASCII — overlaid with YOLOv8x detection across 601 classes, face recognition, body and hand pose skeletons, OCR, gesture/expression/activity recognition, and 60 Hz tracked motion smoothing between 5 Hz YOLO refreshes.

**Developer Tooling**

**[Claritas](https://github.com/KofTwentyTwo/Claritas)** &nbsp;—&nbsp; IntelliJ plugin that transforms messy comments and incomplete Javadocs into structured documentation. PSI-based analysis enforces team standards while preserving content and keeping every transformation safely reversible — comment flowerboxing with configurable borders and width, Javadoc generation from method signatures, file-wide formatting in a single undo action. Multi-module Gradle: a pure Kotlin core library and a thin IntelliJ adapter, so the formatting logic can be reused in CLI tools or other editors later.

**[limen](https://github.com/KofTwentyTwo/limen)** &nbsp;—&nbsp; *threshold.* The two-stage terminal launcher TUI that runs before tmux: pick a host (localhost or a declared SSH target) with live reachability dots and session counts, then pick a session to attach or create. Press `Esc` at any point and `limen` drops you into a fresh unnamed session at the appropriate host. No deliberation tax. Single JSON file declares the fleet. Go + Bubble Tea; installs via Nix or Homebrew tap.

**[obsidian-penny](https://github.com/KofTwentyTwo/obsidian-penny)** &nbsp;—&nbsp; PENNY — Prose Engine for Narrative, Notes, and Yarns. AI co-author for Obsidian: drop annotations like `%% REWRITE: more tension here %%` into a chapter and PENNY rewrites the passage against your style guide and voice tests, then saves a new numbered version (`ch-05.v2.md`) and writes a review file summarizing what changed. Routes by task complexity — CUT and PACING can ride a fast/cheap model while REWRITE and DIALOG go to the strongest. Anthropic API, Ollama, or both.

---

### Writing & Projects

Longer-form essays and project notes live at [kof22.com](https://www.kof22.com):

- **[Blogs](https://www.kof22.com/blogs)** &nbsp;—&nbsp; essays, notes, and the occasional opinion.
- **[Projects](https://www.kof22.com/projects)** &nbsp;—&nbsp; the work behind what's in this README, in longer form.

---

St. Louis &nbsp;·&nbsp; [kof22.com](https://www.kof22.com) &nbsp;·&nbsp; [LinkedIn](https://linkedin.com/in/james-maes) &nbsp;·&nbsp; [Mastodon](https://mastodon.social/@koftwentytwo)
