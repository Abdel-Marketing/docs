# 🗄 Authentication

**Status:** ✅ Live  
**Area:** Infrastructure  
**Owner:** _TBD_

---

## Overview

Every app built with LaunchPulse V2 ships with **built-in authentication**. You don't have to wire up an auth provider, set up session handling, or build login screens from scratch — the agent connects auth as part of the build, and you can ask for the flow you want in plain English.

---

## What's supported (intended baseline)

- **Email + password** sign-up and login
- **Magic-link / passwordless** flows
- **Social login** (Google, Apple, etc.)
- **Session management** (tokens, refresh, sign-out)
- **Gated routes / screens** based on auth state
- **Role-based access** when paired with Custom Agents or paid-feature gating

---

## How you ask for it

Like everything else in LaunchPulse, you describe what you want:

- "Add Google sign-in to my app."
- "Require login before users can access the dashboard."
- "Add email + password auth with a forgot-password flow."
- "Lock the admin section to one specific email."

The agent then implements the screens, the backend logic, and the gating across the app.

---

## How it pairs with payments

Auth and Payments work together: once a user is signed in, paywalls and Pro-feature gates (via Stripe / RevenueCat) can be applied to that user's account automatically. See the Payments page.

---

## What's missing / TODO

- [ ] Publish a complete list of supported auth providers
- [ ] Document MFA / 2FA support
- [ ] Add SSO (SAML / OIDC) for team / enterprise apps
- [ ] Document password reset and account-deletion flows
- [ ] Clarify where user records live (which DB / schema)
