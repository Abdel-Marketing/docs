# 🧠 AI Multi-Agent Mode

**Status:** 🚧 In progress  
**Area:** Build Engine  
**Owner:** _TBD_

---

## Overview

Multi-Agent Mode is an alternative to the single Autonomous AI Software Engineer. Instead of one agent handling everything, the work is split across **specialised agents** that collaborate on the build:

- a **Planner** agent (scopes the build and breaks it into tasks)
- a **Builder** agent (writes and edits code)
- a **Reviewer** agent (checks quality, catches regressions)
- a **QA / Testing** agent (runs and validates checks)

Multi-Agent Mode is useful when a project is large enough that one agent loses context, or when you want stronger separation between "execution" and "review."

---

## How it works (intended)

1. User selects **AI Multi-Agent Mode** at project creation.
2. The Planner agent produces the build plan + feature list.
3. The user approves / edits the plan (same control surface as Autonomous mode).
4. Builder and Reviewer agents work in a loop until each feature passes QA.
5. The user sees per-agent progress in the workspace.

---

## What's missing / TODO

- [ ] Finalise the agent handoff protocol (planner → builder → reviewer)
- [ ] Decide which agents are user-configurable vs fixed
- [ ] Add per-agent activity feed in the UI
- [ ] Document credit cost difference vs Autonomous mode
- [ ] Write the public-facing intro doc (currently only mentioned in passing)

---

## Open questions

- Can users swap one of the default agents for a Custom Agent they built?
- Should Multi-Agent Mode default to a stronger reasoning model?
- How is conflict resolved when Builder and Reviewer disagree repeatedly?
