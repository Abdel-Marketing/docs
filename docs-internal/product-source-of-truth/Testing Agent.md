# 🧪 Testing Agent

**Status:** 🚧 In progress  
**Area:** Build Engine  
**Owner:** _TBD_

---

## Overview

The Testing Agent is a built-in agent dedicated to **quality assurance** during and after a build. While the Autonomous AI Software Engineer already runs basic checks as it builds, the Testing Agent goes further: it generates test plans, runs them against the live preview, and reports failures back into the build loop so they can be fixed automatically.

This sits alongside the existing "quality assurance baked into the workflow" promise — but makes it explicit, visible, and configurable.

---

## What it does (intended)

- Reads the approved feature list and **generates a test plan per feature**
- Runs **happy-path, edge-case, and failure-path** checks
- Surfaces failed tests in the workspace with reproduction steps
- Optionally feeds failures back to the Builder agent so they get fixed before the next iteration
- Produces a final **QA report** before deployment

---

## Why it matters

- Catches regressions introduced by later iterations
- Prevents shipping broken flows to App Store / Play Store / production web
- Reduces back-and-forth: instead of the user spotting bugs, the agent does

---

## What's missing / TODO

- [ ] Decide whether the Testing Agent runs automatically or on demand
- [ ] Define which test types are in scope at v1 (UI, API, auth, payments?)
- [ ] Document how it interacts with Custom Agents (can a user-built QA agent replace it?)
- [ ] Build the QA report UI
- [ ] Decide credit cost model for test runs

---

## Open questions

- Should test runs block deployment, or just warn?
- Should users be able to write and pin their own test cases?
