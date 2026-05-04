# 🗄 Custom Domain

**Status:** ✅ Live (purchase flow coming soon)  
**Area:** Infrastructure  
**Owner:** _TBD_

---

## Overview

Once your app is built, you can attach a **custom domain** so it goes live under your own URL instead of a default LaunchPulse subdomain. This works for web apps deployed through LaunchPulse hosting.

In the future, you'll also be able to **buy domains directly inside LaunchPulse** — no need to register through a third-party provider first.

---

## How it works today

1. Register a domain with any registrar (or use one you already own).
2. In your project, open the **Custom Domain** settings.
3. Enter the domain you want to attach.
4. LaunchPulse gives you the DNS records to add at your registrar (typically an A record and/or CNAME).
5. Once DNS propagates, LaunchPulse provisions an SSL certificate and your app is live on your domain.

---

## Coming soon: domain purchasing

We're building a flow that lets you **search and buy domains directly inside LaunchPulse**, so the full path looks like:

> Build app → pick a name → buy the domain in-product → deploy → live.

No leaving the workspace, no manual DNS, no second account.

---

## What's missing / TODO

- [ ] Ship the in-product domain purchase flow
- [ ] Document supported TLDs at launch
- [ ] Add automatic DNS configuration when the domain is bought through us
- [ ] Document what happens to a custom domain if a project is deleted
- [ ] Add a "domain health" indicator (DNS OK, SSL OK, redirect OK)
