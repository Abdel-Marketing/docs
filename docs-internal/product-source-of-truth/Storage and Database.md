# 🗄 Storage & Database

**Status:** ✅ Live  
**Area:** Infrastructure  
**Owner:** _TBD_

---

## Overview

LaunchPulse V2 includes **built-in cloud storage** so apps can handle file uploads, downloads, and management without external services like AWS S3. It also manages databases, schemas, configuration, and history behind the scenes — so your projects stay consistent, reproducible, and safe.

You don't manage infrastructure directly, but you _do_ control what's stored, what's deployed, and how environments are configured. The result is the safety of managed infrastructure with the clarity of knowing where everything lives.

---

## What LaunchPulse stores for you

- **Code & assets** — frontend, backend, and generated artefacts for each project and version
- **Application data** — databases and schemas created by the Database Agent or configured in your project
- **Configuration** — environment variables, secrets, and settings required for your app to run
- **Metadata & history** — agent logs, build history, and previous iterations so you can trace how a project evolved

---

## File storage for your app

Built-in cloud storage means uploads, downloads, and file management work out of the box. Your users can upload images, documents, and other files without you wiring up an external bucket.

---

## Environments

Storage is structured to support multiple environments so you can keep development, staging, and production safely separated.

| Environment | Purpose |
| --- | --- |
| Development | Build and iterate without affecting real users |
| Staging | Internal preview / pre-release validation |
| Production | Live data for real users |

---

## Billing

Storage and database usage is **pay-as-you-go** (separate from credits). Small projects stay light; bigger projects scale without forcing everyone into the same flat fee. See the Accounts & Subscriptions page.

---

## What's missing / TODO

- [ ] Publish concrete storage limits per plan
- [ ] Document the database engine(s) used under the hood
- [ ] Add backup / restore guidance
- [ ] Clarify how secrets are encrypted at rest
- [ ] Add an "export my data" flow for users who want a copy
