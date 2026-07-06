<div align="center">

<img src="chrome-mv3/icon/128.png" width="88" alt="EchoSync" />

# EchoSync

**Watch Twitch live streams in perfect sync with your friends.**

Free · open source · no account · runs on your own PC

</div>

---

EchoSync keeps everyone in a watch party lined up on the **same moment** of a live stream. It measures who's ahead or behind and quietly closes the gap on each person's *own* native Twitch player — so the big plays land at the same time instead of seconds apart. No shared screen, no re-streaming; everyone keeps their own full-quality stream.

This repository holds the **ready-to-use downloads**:

| File | What it is |
|------|------------|
| **`echosync-host.exe`** | The host app (Windows). **One** person in the group runs this to create the watch party. |
| **`chrome-mv3/`** | The browser extension, unpacked. **Everyone** who watches installs this. |

---

## Contents

- [How it works in 30 seconds](#how-it-works-in-30-seconds)
- [What you need](#what-you-need)
- [Step 1 — Download the files](#step-1--download-the-files)
- [Step 2 — Install the extension](#step-2--install-the-extension)
- [Step 3 — Host a watch party](#step-3--host-a-watch-party)
- [Step 4 — Everyone joins](#step-4--everyone-joins)
- [Stopping the party](#stopping-the-party)
- [Troubleshooting](#troubleshooting)
- [FAQ](#faq)

---

## How it works in 30 seconds

1. **One person hosts.** They run `echosync-host.exe` and click **Start**. It creates a private link.
2. **Everyone installs the extension** and pastes that link.
3. On any Twitch stream, the EchoSync overlay shows who's ahead or behind.
4. Click **Align everyone** — everybody snaps to the same moment. 🎉

> You only ever need **one** host. Everyone else just needs the extension and the link.

---

## What you need

- **The host:** Windows 10 or 11 (that's what `echosync-host.exe` runs on) and an internet connection.
- **Everyone, including the host:** Google Chrome — or any Chromium browser (Edge, Brave, Opera).

---

## Step 1 — Download the files

The easiest way to grab everything at once:

1. At the top of this page, click the green **`< > Code`** button → **Download ZIP**.
2. Save it somewhere you'll find it (your Desktop is fine).
3. **Unzip it:** right-click the downloaded `.zip` → **Extract All…** → **Extract**.

You'll end up with a folder containing **`echosync-host.exe`** and the **`chrome-mv3`** folder — those are the only two things you need.

> 💡 Want just one file instead? Click a file above (e.g. `echosync-host.exe`) and use the **download** button. But the full ZIP is simplest, because it also gives you the `chrome-mv3` folder you may need in Step 2.

---

## Step 2 — Install the extension

**Everyone who wants to watch together does this — including the host.**

### Option A — Chrome Web Store *(recommended)*

<!-- ▼▼▼ TODO: paste your published Chrome Web Store URL between the parentheses below, then delete this comment ▼▼▼ -->

> 🧩 **[➕ Add EchoSync to Chrome](REPLACE-WITH-CHROME-WEB-STORE-LINK)**
>
> *(Chrome Web Store listing — link coming soon.)*

One click, and it stays up to date automatically. Use this once the listing is live.

### Option B — Load the `chrome-mv3` folder *(fallback)*

> ⚠️ **Use this only if the Chrome Web Store version above isn't available yet, or isn't working for you.** It is the **exact same extension** — just installed manually from the folder in this repo.

1. Make sure you've downloaded and unzipped this repo ([Step 1](#step-1--download-the-files)) so you have the **`chrome-mv3`** folder.
2. Open Chrome and go to **`chrome://extensions`** (type it into the address bar and press Enter).
3. Turn on **Developer mode** — the toggle in the **top-right** corner.
4. Click **Load unpacked** (top-left).
5. Select the **`chrome-mv3`** folder, then click **Select Folder**.
6. EchoSync now shows up in your list. Click the puzzle-piece 🧩 icon in the toolbar and **pin** EchoSync so it's always one click away.

> 📌 **Keep the folder where it is.** Chrome loads the extension straight from that folder on disk. If you move or delete it, the extension stops working — if you ever do move it, just run **Load unpacked** again and point it at the new location.

---

## Step 3 — Host a watch party

**Only one person does this.** If you're joining someone else's party, skip ahead to [Step 4](#step-4--everyone-joins).

**1. Run `echosync-host.exe`** — just double-click it.

<details>
<summary>💬 Got a "Windows protected your PC" message? (click to expand)</summary>

<br>

EchoSync is a small open-source app and isn't code-signed, so Windows SmartScreen may show a blue warning the first time you run it. This is normal for indie apps. Click **More info**, then **Run anyway**.

</details>

**2.** A small **EchoSync Host** control panel opens. There's no console or terminal window — that's intended; the panel *is* the app.

**3. Click Start.** The very first time, it downloads a tiny networking helper (Cloudflare's `cloudflared`), so give it a few seconds and make sure you're online.

**4.** Once it's hosting, the panel shows **two** links:

| Link | Who uses it |
|------|-------------|
| **Friends paste this link** — a public `…trycloudflare.com` URL | **Send this to your friends** (Discord, text, wherever). |
| **On this PC (you) paste this instead** — `http://localhost:8787` | **You**, the host, use *this* one in your own browser. |

> 🏎️ **Host: use the localhost link for yourself.** The public link travels out over the internet — great for friends, but routing *your own* traffic out and back can slow your stream down. On the hosting PC, use `http://localhost:8787` to keep your video buttery-smooth.

> 🔗 **The public link is new every time you host.** Each session generates a fresh URL, so share the current one at the start of each watch party.

---

## Step 4 — Everyone joins

Everyone in the party (the host too) does this on the stream you're watching together:

1. Open the stream on **twitch.tv**.
2. Click the **EchoSync** icon in your toolbar.
3. Type a **nickname** — how your friends will see you.
4. Paste the **link**:
   - **Friends** → the **public link** the host sent you.
   - **The host** → your own **`http://localhost:8787`** link.
5. Click **Join**.

The EchoSync overlay appears right on the stream. Whenever someone drifts out of sync, click **Align everyone** (or **Align me** for just yourself) and everybody snaps back to the same moment. That's it — enjoy watching together. 🎉

---

## Stopping the party

- **Host:** close the EchoSync Host panel window. That stops hosting and shuts everything down cleanly — nothing is left running in the background.
- **Watchers:** click **Leave** in the popup, or simply close the Twitch tab.

---

## Troubleshooting

<details>
<summary><b>"Windows protected your PC" when I run the host app</b></summary>

<br>

Expected — the app isn't code-signed. Click **More info** → **Run anyway**. If you'd rather verify it yourself first, the full source is public (see the [FAQ](#faq)).

</details>

<details>
<summary><b>My own stream is laggy while I'm hosting</b></summary>

<br>

In your browser, use the **`http://localhost:8787`** link, **not** the public one. The public link routes your traffic out to the internet and back, which can slow your video down. The panel labels this link *"On this PC (you) paste this instead."*

</details>

<details>
<summary><b>The sync overlay isn't showing up on Twitch</b></summary>

<br>

Open the EchoSync popup and make sure **Show sync panel** is switched on — toggling it on also parks the panel neatly in the **top-left** corner in case it drifted off-screen. If it still doesn't appear, **reload the Twitch tab**.

</details>

<details>
<summary><b>My antivirus flagged echosync-host.exe</b></summary>

<br>

It's an unsigned, self-contained binary, which some antivirus engines flag by default even when there's nothing wrong. EchoSync is open source — you can review the code or build the app yourself (see the [FAQ](#faq)). Allow it or add an exception if you trust it.

</details>

<details>
<summary><b>I can't reopen the host app / "port already in use"</b></summary>

<br>

Make sure a previous EchoSync Host isn't still running — check the system tray and, if needed, **Task Manager** for `echosync-host.exe`. Close it, then start again.

</details>

<details>
<summary><b>My friends can't connect</b></summary>

<br>

Double-check they're pasting the **current** public link (it changes every session) and that you've clicked **Start**. Have one friend re-copy the latest link straight from your panel.

</details>

<details>
<summary><b>The extension won't install from the Chrome Web Store</b></summary>

<br>

Use **[Option B](#option-b--load-the-chrome-mv3-folder-fallback)** — load the `chrome-mv3` folder manually. It's the same extension.

</details>

---

## FAQ

**Is it really free?**
Yes — completely. No account, no subscription, no catch.

**Does my video go through the host's PC?**
No. Your stream comes straight from Twitch, exactly as it always does. EchoSync only passes tiny timing and nickname messages between the party, so your video quality is never touched.

**Do my friends need the host app too?**
No. Only the **one** host runs `echosync-host.exe`. Everyone else just needs the extension and the link.

**Can the host run on Mac or Linux?**
The prebuilt host here is Windows-only. Your friends can be on any operating system — they only need the browser extension. (Building the host for other platforms is possible from the source.)

**Is my data private?**
Yes. No ads, no analytics, no tracking. The party runs on the host's own PC, not on anyone else's cloud, and the only thing that leaves your machine is small sync data shared with your party.

**Where's the source code?**
EchoSync is open source: **https://github.com/AceeEcho/EchoSync**

---

<div align="center">

Made for watch parties that actually stay in sync. 💙

</div>
