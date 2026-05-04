# 👥 Collaboration

**Status:** ✅ Live  
**Area:** Team  
**Owner:** _TBD_

---

## Overview

LaunchPulse V2 supports **team collaboration**, so multiple users can work on the same project without duplicating work or losing context. Share a project with other members and control what they're allowed to do — whether they're there to **review** progress or **make changes**.

---

## How collaboration works

### Share a project with your team
Invite teammates to the same project so they can jump in and contribute during iteration.

Common uses:
- a co-founder continues the build while you're offline
- a developer fixes bugs while you focus on product
- a mentor reviews progress without editing anything
- a designer checks UI and leaves feedback

---

## Permission levels

LaunchPulse V2 keeps permissions simple and practical.

### 👁 Viewer (overview)
Best for people who should:
- view the project status
- inspect progress and outputs
- keep track of decisions

Use this for mentors, stakeholders, or anyone reviewing.

### ✏️ Editor (can edit)
Best for collaborators who should:
- make changes to the project
- iterate on features
- contribute to the build workflow

Use this for teammates actively working on the product.

---

## Best practices

- Give people the **minimum access they need** (viewer vs editor) to keep projects safer and cleaner
- Use **viewer** for reviews and feedback loops
- Use **editor** only for people who will actually ship changes
- Create task-focused **Custom Agents** for the team (QA agent, Code Reviewer, PM agent) so collaboration stays consistent

---

## Quick examples

- "Invite my cofounder as an editor."
- "Give my mentor view-only access."
- "Add a teammate to help iterate on the onboarding flow."

---

## What's missing / TODO

- [ ] Add an Admin / Owner role distinct from Editor
- [ ] Add per-file or per-feature permissions for larger teams
- [ ] Add an activity feed showing who changed what
- [ ] Add @mentions and inline comments
- [ ] Document the credit-cost model for shared projects (whose credits get used?)
