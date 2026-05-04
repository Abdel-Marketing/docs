# 🛠 Troubleshooting

**Status:** 🚧 In progress  
**Area:** Support  
**Owner:** _TBD_

---

## Overview

Common issues users hit in LaunchPulse V2 and how to resolve them. This page is a living document — add new entries as patterns emerge from support.

---

## Build issues

### The build is stuck or has stopped responding
- Refresh the workspace and reopen the project
- Check your credit balance — the build pauses if credits run out
- If still stuck, restart the build from the last approved plan step

### The agent built something different from what I asked for
- Open the plan view and **add context** explaining what you actually want
- Re-prompt with concrete examples ("like X but with Y")
- Use a **Custom Agent** (e.g. PM Agent) to tighten the spec before building

### The live preview isn't updating
- Check the build log for errors
- Hard-refresh the preview pane
- Confirm the latest iteration finished (not just started)

---

## Credits and billing

### I ran out of credits mid-build
- Buy a **credit add-on** to keep going without waiting for the next billing cycle
- See [Accounts & Subscriptions](Accounts%20and%20Subscriptions.md)

### I was charged for storage / database
- Storage and database are **pay-as-you-go**, separate from credits
- Review usage in your account area

---

## Deployment issues

### My iOS publish failed
- Confirm your Apple Developer membership is active
- Double-check the **Bundle ID** matches what's in App Store Connect
- Use an **app-specific password**, not your main Apple Account password
- Make sure the Apple Team ID is correct if your account is on multiple teams

### My Android publish failed
- Confirm the **service account JSON** is valid and has Play Console upload permissions
- Make sure the **Package name** matches the existing Play Console app (if reusing one)
- Try the **Internal** track first to validate the upload pipeline

### My custom domain isn't going live
- DNS propagation can take up to 24 hours — check again later
- Confirm the A / CNAME records at your registrar match what LaunchPulse provided
- Make sure SSL has provisioned (LaunchPulse handles this automatically once DNS resolves)

---

## Auth / payments

### Login isn't working in the live app
- Confirm the auth provider (Google, email, etc.) was actually wired in — re-prompt the agent if not
- Check that the user record exists in the database
- For social login, confirm the OAuth credentials are configured

### Payments aren't going through
- For web: confirm Stripe is connected and test mode is off when going live
- For mobile: confirm RevenueCat products match the App Store / Play Store entries
- Test with a sandbox account before going live

---

## Collaboration

### A teammate can't see my project
- Confirm you invited them with at least **Viewer** access
- Ask them to refresh and check the Projects sidebar

### A teammate's edits overwrote mine
- Use **Viewer** access for people who shouldn't be making changes
- Coordinate big iterations in chat/Slack to avoid simultaneous edits

---

## Still stuck?

- Check the relevant feature page in this roadmap
- Reach out to LaunchPulse support with your project ID and a description of the issue

---

## What's missing / TODO

- [ ] Add error-code reference table once codes are standardised
- [ ] Add screenshots for the most common failure states
- [ ] Add a "report a bug" form linked from this page
- [ ] Add per-feature troubleshooting deep-dives
