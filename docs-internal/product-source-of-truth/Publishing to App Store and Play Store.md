# 🚢 Publishing to App Store & Play Store

**Status:** ✅ Live  
**Area:** Deployment  
**Owner:** _TBD_

---

## Overview

LaunchPulse V2 supports **direct publishing to the Apple App Store and Google Play Store** from inside the platform. Instead of exporting builds, opening multiple dashboards, and manually uploading binaries, you can "vibe code" the release:

1. tell the agent you want to publish
2. fill a small set of store details
3. click **Start publish**
4. LaunchPulse handles the **build + submission** flow

---

## The vibe-coding workflow

### 1) Prompt the agent
- "Publish my app to the App Store."
- "Deploy to Play Store (internal testing)."
- "Publish iOS + Android."

### 2) LaunchPulse opens the Publish modal
You choose:
- ✅ **Publish iOS (App Store)**
- ✅ **Publish Android (Play Store)**

### 3) Fill the required store fields
LaunchPulse asks only for what's needed to build and submit.

### 4) Click "Start publish"
LaunchPulse runs the build and submits binaries to the selected store(s).

---

## Under the hood

LaunchPulse's publishing flow follows the same pattern used in Expo's production pipeline:

- **Build step** — generates store-ready binaries (iOS `.ipa`, Android `.aab`) and handles signing
- **Submit step** — uploads binaries to **App Store Connect** and **Google Play Console**

You don't manage build machines, signing setup, or upload tooling manually.

---

## iOS (App Store) settings

| Field | What it is |
| --- | --- |
| **Bundle ID** (`com.company.app`) | Unique identifier. Use your domain naming style. Hard to change once live — choose carefully. |
| **App name** | Display name shown in the App Store. |
| **App Store Connect App ID** _(optional)_ | Numeric ID for an existing app record. Leave blank to let LaunchPulse auto-create it. |
| **Apple ID (email)** | Apple Account email with App Store Connect access. |
| **Apple ID password** | Use an **app-specific password** — safer than your main account password. |
| **TestFlight groups** _(optional, comma-separated)_ | e.g. `Internal Testers, Beta Users` |
| **Apple Team ID** _(optional)_ | Useful when your Apple account is linked to multiple teams. |
| **Submit for App Store review** | **Off:** upload only. **On:** also submit for Apple review (best when metadata + screenshots are ready). |

---

## Android (Play Store) settings

| Field | What it is |
| --- | --- |
| **Package name** (`com.company.app`) | Android's unique identifier. |
| **Track** | Where the release goes — e.g. **Internal** for quick testing with a small tester list. |
| **Play Store service account JSON** | A JSON key for a Google service account with permission to upload to your Play Console. Required because Google Play uses service accounts (Android Publisher API) for automated uploads. |

---

## Pre-publish checklist

**For iOS**
- Apple Developer Program membership
- App Store Connect access for the Apple account you'll use
- Bundle ID chosen

**For Android**
- Google Play Developer account
- A Google Cloud service account + JSON key
- Service account granted the right permissions in Play Console

---

## Result

Once you click **Start publish**, LaunchPulse:
- builds store-ready binaries
- applies the required signing/submission flow
- submits to the store(s) you selected
- puts you on the fastest path to TestFlight / Internal testing / production release

---

## What's missing / TODO

- [ ] Document failure modes (what happens if Apple rejects)
- [ ] Add a "publish history" view per project
- [ ] Support promoting a build between tracks (Internal → Production)
- [ ] Auto-generate store screenshots from the live preview
