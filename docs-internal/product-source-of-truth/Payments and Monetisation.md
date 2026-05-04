# 💳 Payments & Monetisation

**Status:** ✅ Live  
**Area:** Monetisation  
**Owner:** _TBD_

---

## Overview

Every app built with **LaunchPulse V2** is **payment-ready** by default. You can start monetising without spending days on payment setup, edge cases, or complex integrations.

LaunchPulse V2 supports smooth payment and subscription flows through:

- **Stripe** (web)
- **RevenueCat** (mobile — App Store / Play Store)

---

## Why this matters

Payments are usually one of the slowest parts of shipping an app:
- multiple tools to connect
- lots of setup steps
- subscription logic and edge cases
- testing and verification

LaunchPulse V2 removes most of that work by letting the agent implement monetisation for you.

---

## How it works

### 1) You prompt monetisation in plain English
Instead of manually wiring payment logic, you describe what you want.

> **"Add a $10 subscription to my app."**

### 2) The agent builds the payment flow end-to-end
Once you request monetisation, the LaunchPulse agent handles:
- creating the subscription / pricing model
- connecting your app to the payment provider(s)
- adding the paywall or checkout experience
- gating features based on subscription status
- ensuring the app can collect revenue correctly

You get a working, testable flow without doing the integration yourself.

---

## Common monetisation prompts

- "Add a monthly subscription for $10."
- "Add annual and monthly plans."
- "Add a free plan + Pro plan."
- "Lock these features behind the paid plan."
- "Add a one-time payment option."

---

## What "payment-ready" means

- Monetisation can be added **immediately**
- You don't manually stitch together Stripe + subscription logic
- The agent implements payments as part of the build, just like any other feature
- Mobile apps get RevenueCat wired up so IAP works in TestFlight + Play internal testing

---

## What's missing / TODO

- [ ] Document supported currencies and tax handling
- [ ] Add a built-in revenue dashboard (or link out to Stripe/RevenueCat)
- [ ] Support promo codes and trials out of the box
- [ ] Document refund / cancellation flows
- [ ] Add prebuilt paywall templates the agent can pick from
