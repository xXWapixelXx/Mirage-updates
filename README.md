<!-- ░░░ Mirage ░░░ -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=240&color=gradient&customColorList=12,17,20&text=Mirage&fontSize=78&fontColor=ffffff&fontAlignY=38&desc=Teleport%20your%20iPhone%27s%20location%20—%20anywhere&descSize=18&descAlignY=60&animation=fadeIn" alt="Mirage" width="100%"/>

<a href="https://github.com/xXWapixelXx">
  <img src="https://readme-typing-svg.demolab.com?font=Rubik&weight=600&size=24&duration=3200&pause=700&color=6C5CE7&center=true&vCenter=true&width=560&lines=Real+GPS+override+%E2%80%94+on-device;No+computer+needed+%E2%80%94+at+all;No+Wi-Fi+needed+%E2%80%94+works+on+5G;Walk%2C+drive+or+ride+the+bus;Private+by+design+%E2%80%94+nothing+leaves+your+phone" alt="typing" />
</a>

<br/>

![iOS](https://img.shields.io/badge/iOS-27-000000?style=for-the-badge&logo=apple&logoColor=white)
![SwiftUI](https://img.shields.io/badge/SwiftUI-native-1575F9?style=for-the-badge&logo=swift&logoColor=white)
![Privacy](https://img.shields.io/badge/privacy-on--device-2FE6A8?style=for-the-badge)
![Version](https://img.shields.io/badge/version-3.4.1-8E7BEF?style=for-the-badge)
![No PC](https://img.shields.io/badge/no%20computer-required-2ECC71?style=for-the-badge)

<sub>iOS 18 → 27 · tested on iOS 27 & iPhone 17 Pro · made by Wapixel</sub>

</div>

---

## ✦ What is Mirage?

Mirage makes your iPhone believe it's somewhere else. Drop a pin anywhere on the
map, tap **Teleport**, and every app reads that location — not a fake wrapper,
the real system location. Walk around with a joystick, follow a route you draw,
or import a GPX track and let Mirage travel it for you.

Clean, fast, maps-first SwiftUI. No ads, no tracking, nothing leaves your phone.

## ✦ Two ways to spoof

Mirage ships **two engines** — pick whatever fits how you installed it.
**Neither one needs a computer on iOS 27.**

| Mode | What it does | Needs | Best for |
|------|--------------|-------|----------|
| 🛰️ **GPS override** | Overrides the *real* satellite GPS — the strong one | **No computer on iOS 27** — Mirage makes its own pairing file (iOS 18–26: one-time computer step) + a tunnel (built-in on paid signing, or the free **LocalDevVPN** app) | Everything, incl. GPS-only apps |
| 📶 **WiFi mode** | Rewrites the WiFi/coarse location lookup — **no pairing file at all** | Mirage's own VPN (paid signing) + a trusted cert (installed on-device) | Quick setup, indoor / coarse location |

> **Free sideload?** Mirage detects it automatically and switches to the
> external **LocalDevVPN** tunnel — it never asks you to run a VPN it can't.

## ✦ Features

|   |   |
|---|---|
| 🔓 **No computer needed** | On iOS 27 Mirage pairs with your iPhone itself. No Mac, no PC, no cable. |
| 📍 **Real GPS override** | Beats plain WiFi tricks — overrides the actual satellite GPS. |
| 📶 **No Wi-Fi needed** | **New in 3.1** — spoof on mobile data. On an external tunnel, flick Mobile Data off for a few seconds to connect, then turn it straight back on. |
| 🚌 **Public transport** | **New in 3.1** — bus, tram, metro and train that actually stop at stops, alongside walk / run / cycle / drive. |
| 💾 **Pairing backups** | **New in 3.1** — your pairing file is saved to Files and can be shared off the phone, so reinstalling never means redoing it. |
| ↩️ **Backtrack** | **New in 3.3** — a spoof remembers where it began, so *Back to <place>* takes you home the way you came. |
| 📤 **Share a pin** | **New in 3.3** — hand off any spot's coordinate and a Maps link straight from the place card. |
| 🔒 **Steer from the Lock Screen** | **New in 3.4** — turn, go/hold, pace and stop live on the Lock Screen and Dynamic Island, so you can move your location without opening the app. |
| ☁️ **Saved places sync** | **New in 3.4** — favourites back up to your account and appear on your other devices. Renames and deletions travel too. |
| 🕹️ **Live joystick** | Move your location in real time, and change pace mid-journey. |
| 🗺️ **Routes + GPX** | Tap or draw a path, follow it automatically, import & export GPX. |
| 🌗 **Light & dark** | Auto / Light / Dark, with light mode mixed for paper rather than inverted. |
| 🔔 **Live Activity** | Place, speed, distance and link health on the Lock Screen and Dynamic Island. |
| 🌍 **Map your way** | Standard / Hybrid / Satellite, world search, favourites and recents. |
| 💓 **Self-healing link** | Health monitor re-applies a dropped spoof; resumes after an accidental close. |
| 🔒 **On-device & private** | No location history uploaded, no third-party analytics. |

## ✦ Screenshots

<div align="center">

<table>
  <tr>
    <td align="center" width="50%">
      <img src="docs/screenshots/map.png" width="260" alt="Map" /><br/>
      <sub><b>Map</b> — the whole world, one tap away</sub>
    </td>
    <td align="center" width="50%">
      <img src="docs/screenshots/location-drop.png" width="260" alt="Drop a pin" /><br/>
      <sub><b>Drop a pin</b> — teleport, save or share</sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <img src="docs/screenshots/walk-route.png" width="260" alt="Walk a route" /><br/>
      <sub><b>Walk a route</b> — draw a path and stroll it</sub>
    </td>
    <td align="center" width="50%">
      <img src="docs/screenshots/settings.png" width="260" alt="Settings" /><br/>
      <sub><b>Settings</b> — engines, tunnel &amp; live status</sub>
    </td>
  </tr>
</table>

<sub>iPhone 17 Pro · iOS 27</sub>

</div>

## ✦ Compatibility

- **iOS 18 → 27** — tested on the **iOS 27 beta** and **iPhone 17 Pro**.
- GPS override uses Apple's developer location service (iOS 17.4+); WiFi mode
  needs Mirage's own VPN (paid signing).
- Installed via sideloading (SideStore / AltStore, or a signed build). Paid
  signing unlocks the built-in VPN; a free sideload uses the LocalDevVPN tunnel.
- GPS override needs a **pairing file**. On **iOS 27** Mirage creates it on the
  phone; on iOS 18–26 it's a one-time computer step — see **[SETUP.md](SETUP.md)**.

## ✦ Setup

Installing takes seconds.

**On iOS 27 — nothing else needed.** Open Mirage → *Pair on this iPhone*, then
confirm the 6-digit code in Settings › Privacy & Security › Developer Mode.
That's the whole setup.

**On iOS 18–26** GPS override still needs a one-time pairing step on any
computer (Mac, Windows or Linux — once per device, reusable forever, no
jailbreak). Full walkthrough → **[SETUP.md](SETUP.md)** · **[pairing guide](PAIRING-WINDOWS.md)**

> ⚠️ It has to be an **RPPairing** file. A `.mobiledevicepairing` from
> SideStore/StikDebug is the older *lockdown* format and won't work.

## ✦ Getting access

Mirage is **invite-only**. Want in?
https://discord.gg/9c29app56C

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-@xXWapixelXx-181717?style=for-the-badge&logo=github)](https://github.com/xXWapixelXx)
&nbsp;
![Discord](https://img.shields.io/badge/Discord-wapixel-5865F2?style=for-the-badge&logo=discord&logoColor=white)

</div>

---

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&section=footer&height=120&color=gradient&customColorList=12,17,20" width="100%"/>

<sub>Mirage · a Wapixel project · not affiliated with Apple</sub>
</div>
