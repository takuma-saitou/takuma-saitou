# Takuma Saitou

*Updated 2026-04-30*

🛰️ A self-bootstrapping multi-agent system, built solo as my primary dev environment. The agents build the system that orchestrates them.

Nearly all my token consumption goes into one piece of software, and that software writes most of itself. Public release is gated on sustained throughput, not a date.

[![Tokscale Stats](https://tokscale.ai/api/embed/takuma-saitou/svg)](https://tokscale.ai/u/takuma-saitou)

## 🤖 What's running

11 agents, 24/7: 1 coordinator, 2 planners, 4 executors, 4 reviewers. Each role swappable across Claude, Codex, Gemini, Qwen, Kimi. Sustained ~9B tokens/day, peaks above 14B.

## 🧬 What it does

A single integrated platform, not a stack of scripts.

**Tasks** are first-class objects with dependencies, kinds, assignees, parent-child trees, configurable review workflows, and acceptance criteria backed by custom programmatic checks. Status changes cascade automatic notifications across the fleet, with aggregate reviews over task trees and built-in reminders.

**Agents** get full lifecycle management with per-agent and shared startup config, sidecar-mode live status, pattern-based output matchers, and fine-grained templates. Hundreds of hook points wire everything together. A TUI scales transparently across the fleet; web-based terminal control adds real-time updates, attachment diff, and React-rendered previews.

**Operations** include a unified async messaging layer, a topic system for structured discussion, an error pipeline that auto-routes failures back into the task queue, blue-green deployment with atomic swaps, bundle distribution, multi-project orchestration, and a standalone watchdog.

## 📈 How it grew

| Week | Tokens/day | Tasks done | Commits | Reject rate | What changed |
|------|------------|-----------|---------|-------------|--------------|
| Feb 15–21 | 0.15B | 409 | 189 | — | 🌱 Initial bootstrap |
| Feb 22–28 | 0.24B | 310 | 260 | — | |
| Mar 1–7 | 0.16B | 341 | 208 | — | |
| Mar 8–14 | 0.75B | 179 | 155 | — | ⚡ Parallel Claude Code orchestration brought online |
| Mar 15–21 | 0.74B | 81 | 701 | 50% | 🔧 Orchestration paused for a full core refactor |
| Mar 22–28 | 0.90B | 3 | 704 | — | |
| Mar 29–Apr 4 | — | 0 | 141 | — | 🔧 Refactor ongoing: core framework split, classification of all major files, 50+ check scripts, pyright strict, ruff |
| Apr 5–11 | — | 48 | 155 | 51% | ✅ Core refactor complete (~60k LOC reworked) |
| Apr 12–18 | 5.45B | 256 | 1,244 | 42% | 🚀 Feature work resumed on the rebuilt core; test count grew from 4k to 11k |
| Apr 19–25 | 10.23B | 346 | 3,818 | 47% | 🔥 Peak week: in-house terminal and TUI, runtime abstraction, networking layer, single-project to multi-project integration |
| Apr 26–30 | 6.62B | 112 | 1,605 | 53% | ⏳ Ongoing |

Across the 75 days: **2,085 tasks completed**, **9,180 commits**, **47% review rejection rate** — nearly half of agent output gets pushed back on the first pass. Historical growth has been **5×/month**; the forward target is a deliberately conservative **3×/month**. Codebase ~**500K lines**, mostly written by the system itself.

Stack started as pure Python, now layered. April brought a Rust core — seven crates for terminal emulation, token tracking, and a typed HTTP/WebSocket client. Frontend is React/TypeScript. All three languages share generated code from a single OpenAPI schema. Quality gate: **200+ project-specific checks** across ~50 scripts, plus 80 incremental migrations.

## 🎯 Where it's going

My personal ceiling — bounded by what I can fund alone — is a sustained **20–30B tokens/day**. That's the ship trigger. Beyond release, the project-level milestone is **1T tokens/day before year end**, combining the system itself plus everyone running it. Pre-release focus: cross-cluster federation, TUI, runtime abstraction, networking, multi-project orchestration.

## 👤 Background

Former CTO and VPoE at a publicly listed company. Independent since. Based in Japan 🇯🇵.

Outside of building, I spend time on philosophy, physics, mathematics, cosmology, geopolitics, and capital markets.

---

⭐ Follow along if you want to watch the system cross 20–30B/day and ship.