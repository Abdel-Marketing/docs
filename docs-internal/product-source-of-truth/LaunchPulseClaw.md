# 🧩 LaunchPulseClaw

**Status:** 🆕 New  
**Area:** Extensions  
**Owner:** _TBD_

---

## Overview

**LaunchPulseClaw** is LaunchPulse's hosting layer for **OpenClaw** agents. You can create your own OpenClaw agent and host it directly with LaunchPulse — no separate infrastructure, no extra deployment pipeline. It plugs into the same workspace, billing, and project model as the rest of LaunchPulse.

This is for users who want to go beyond Custom Agents and build something more capable, more persistent, or more publicly accessible.

---

## How it differs from Custom Agents

| | Custom Agents | LaunchPulseClaw |
| --- | --- | --- |
| Lives inside | A single project workspace | Hosted as its own agent |
| Best for | Reusable helpers during a build (Code Reviewer, QA, PM) | Standalone agents you want to run, share, or expose externally |
| Configuration | Prompt + tools + model | Full OpenClaw agent definition |
| Hosting | Runs inside LaunchPulse chat sessions | Hosted with us, addressable as its own service |

---

## What you can do (intended)

- Build an OpenClaw agent locally or inside LaunchPulse
- Host it with LaunchPulse so it's always available
- Connect it to your projects as a tool / collaborator
- Share it with teammates or expose it externally (where supported)

---

## What's missing / TODO

- [ ] Publish the OpenClaw → LaunchPulseClaw deployment guide
- [ ] Document supported runtime / version
- [ ] Define billing model (credits vs flat hosting fee)
- [ ] Add usage analytics (calls, latency, cost)
- [ ] Add a starter template gallery
- [ ] Document auth / access controls for hosted agents
- [ ] Clarify whether hosted Claws can be invoked from outside LaunchPulse

---

## Open questions

- Is LaunchPulseClaw available on both monthly plans, or gated to the higher tier?
- Can a hosted Claw be used as a tool inside a Custom Agent?
- What happens to a hosted Claw if its parent project is deleted?
