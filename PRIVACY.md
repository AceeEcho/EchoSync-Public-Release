# EchoSync — Privacy Policy

_Last updated: July 6, 2026_

> **In short: EchoSync's developer does not collect, receive, store, sell, or share any of your data — ever. There is no server run by the developer, no analytics, no tracking, no cookies, no ads, and no account.**

EchoSync is a browser extension that keeps a group of friends watching the **same Twitch livestream** in sync. This policy explains, plainly, exactly what data the extension touches and where it goes.

---

## The one thing to know

**The developer of EchoSync never receives any of your data.** The extension sends nothing to the developer, and the developer runs no servers, databases, analytics, or logging of any kind. There is nothing for the developer to collect, because none of your data ever reaches the developer.

---

## How EchoSync works (so the rest makes sense)

To sync a watch party, **one person runs the EchoSync host app on their own computer.** Everyone else's extension connects to *that* person's computer using a link they share. All synchronizing happens between you, that host computer, and the other people in your party. The developer is not part of this at any point.

---

## Data stored only on your device — never transmitted

The extension saves the following in your browser's local storage, **on your device only:**

- Your nickname
- The sync-server link you paste in
- Your settings (for example, whether the on-stream sync panel is shown)

This never leaves your browser, except that the server link is used to connect to the party you chose.

---

## Data shared with your watch party — never with the developer

While you are in a watch party, the extension sends the following to the **host's server** (the computer run by whoever is hosting), and it may be relayed to the other members, **so the party can be kept in sync:**

- **Your nickname** — so others can tell who is who
- **The Twitch channel you're watching**
- **Your player's playback position and state** (playing, paused, buffering, ad break)
- **Network timing** (latency), used to measure who is ahead or behind

This information is used **solely, and in real time,** to line everyone up on the same moment of the stream. It is:

- **Never sent to the developer.**
- **Never sold, rented, or shared with any third party.**
- **Not stored by the developer** — the developer has no server or database. The host's server keeps this only in memory while hosting and discards it the moment hosting stops.

---

## What EchoSync does **not** do

- ❌ No collection of your data by the developer — ever
- ❌ No analytics, telemetry, or usage tracking
- ❌ No advertising or ad networks
- ❌ No cookies or fingerprinting
- ❌ No accounts, sign-ups, or logins
- ❌ No selling or sharing your data with third parties
- ❌ Your video is never routed through the extension — it streams straight from Twitch, exactly as always

---

## Permissions the extension uses

- **Storage** — to save your nickname, server link, and settings on your own device.
- **Access to `twitch.tv`** — so the extension can read and gently adjust the Twitch player to keep you in sync. It requests access to no other websites.

Both permissions exist only to make synchronization work. Nothing more is requested.

---

## Children

EchoSync is a general-audience tool. It is not directed to children under 13 and does not knowingly collect information from anyone — the developer collects no information at all.

---

## Changes to this policy

If this policy ever changes, the updated version will be posted at this same page with a new "last updated" date above.

---

## Contact

Questions about privacy? Please open an issue on the EchoSync public release repository:
**https://github.com/AceeEcho/EchoSync-Public-Release**
