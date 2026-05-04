# 🧠 Custom Agents

**Status:** ✅ Live  
**Area:** Build Engine  
**Owner:** _TBD_

---

## Overview

LaunchPulse V2 lets you create **Custom Agents** (subagents) that you can reuse anytime while building and iterating. Instead of re-explaining the same context over and over, build purpose-tuned agents like:

- Code Reviewer
- QA Tester
- Product Manager
- UI Copywriter
- Security Checklist Agent
- Pitch Deck / Marketing Agent

You can create **as many Custom Agents as you want**, each tuned for a specific task.

---

## Why they're useful

- Keep workflows consistent (same standards every time)
- Move faster during iteration (no re-onboarding each chat)
- Split responsibilities (one for code quality, another for product thinking)
- "Fall back" to an expert helper whenever you're stuck

---

## How to create a Custom Agent

Open **Create Custom Agent** and configure:

### 1) Display Name (required)
Short name shown in your workspace. Example: `Code Reviewer`, `Startup PM`.

### 2) Description
One-line summary. Example: "Reviews PRs, finds bugs, and suggests improvements with minimal changes."

### 3) Model Override
- **Default (inherit from chat)**, or
- a specific model (use a strong reasoning model for deep reviews, a fast one for quick helpers)

### 4) Max Tokens
| Range | Best for |
| --- | --- |
| 1,000–3,000 | Fast, short outputs (checklists, quick reviews) |
| 4,000–8,000 | Deeper reasoning (architecture reviews, strategy docs) |
| 10,000+ | Long reports (specs, audits, multi-step plans) |

### 5) Agent Prompt (required)
The agent's "operating manual." A strong prompt includes:
- **Role** (what the agent is)
- **What it produces** (outputs, format)
- **Rules** (do/don't, quality bar)
- **How it handles uncertainty** (ask for missing info, list assumptions)
- **Default structure** for responses

---

## Available Tools

Enable only what the agent needs — focused agents stay predictable.

- **Read Files** — inspect project files before answering
- **Write Files** — generate new files (docs, code, configs)
- **Edit Files** — apply targeted changes to existing files
- **Bash Commands** — run builds, tests, linting
- **Glob Search / Grep Search** — find files or patterns across the repo
- **Web Fetch / Web Search** — pull in up-to-date info or reference docs

**Least-access guidance:**
- **Reviewer agents**: Read + Search (no Write/Edit)
- **Builder agents**: Write/Edit + Read, optionally Bash
- **Research agents**: Web Search + Web Fetch, optionally Read

### MCP Servers (optional)
Attach MCP servers to extend what an agent can do — connecting external systems or internal tools. Leave unconfigured if you don't need it.

---

## Example Custom Agents

### Code Reviewer Agent
**Goal:** catch bugs, improve clarity, keep changes minimal.
- Output: bullet list of issues + suggested patch approach
- Rules: don't rewrite everything, prioritize correctness + readability
- Tools: Read Files, Grep Search

### QA Tester Agent
**Goal:** generate test cases and edge cases.
- Output: test checklist + reproduction steps
- Rules: cover happy path + failure path + security basics
- Tools: Read Files

### Product Manager Agent
**Goal:** refine features, MVP scope, and priorities.
- Output: prioritized backlog + acceptance criteria
- Rules: always separate MVP from "later"

### UI Copywriter Agent
**Goal:** write clean microcopy and onboarding text.
- Output: final copy + variants (short / friendly)
- Rules: simple language, consistent tone

---

## Best practices

- Keep each agent **narrow** (one job, one style)
- Put non-negotiables in the prompt (quality bar, format, rules)
- Create one agent for **execution** (building) and another for **review** (checking)
- If an agent is too verbose, lower Max Tokens and demand a fixed structure

---

## What's missing / TODO

- [ ] Add a public template library users can clone
- [ ] Document how Custom Agents interact with Multi-Agent Mode
- [ ] Add usage analytics per agent (calls, credit cost)
