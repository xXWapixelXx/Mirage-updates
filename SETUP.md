# Mirage — first-time setup

Mirage installs like any sideloaded app, then needs **one** small setup step so
it can override GPS.

## 1. Install the app
Mirage is invite-only — see the [README](README.md) to get access. Install it
with your sideloading tool of choice (SideStore / AltStore, or a signed build).
EU users can install with **AltStore PAL** straight from Safari, no computer.

## 2. Pairing (needed for GPS spoofing)

To set your GPS location, iOS requires a **trust relationship** ("pairing").

### 🔓 On iOS 27 — no computer at all

Mirage can pair with your iPhone by itself. It runs a pairing host on the phone
and your iPhone pairs with it over the local network:

1. Open Mirage → **Settings → Developer login → Pair on this iPhone**
   (or tap **Pair without a computer** in the first-time guide).
2. Allow **Local Network** when asked — that's how your iPhone finds Mirage.
3. Leave Mirage open and go to **Settings › Privacy & Security › Developer Mode
   → Pair with Host**, then pick **Mirage**.
4. Type the **6-digit code** Mirage is showing. Done — you're paired.

> Keep Mirage open while you're in Settings; it has to stay listening.
> If nothing shows up under *Pair with Host*, your iOS version doesn't support
> device-initiated pairing yet — use the computer route below.

### 💻 On iOS 18–26 — one-time computer step

Older versions can't pair themselves, so this is an Apple security step that
can't be done on the phone alone. The good news:

- ✅ **One time only** — the pairing file is reusable forever after.
- ✅ **Any computer** works (Windows, macOS, or Linux) — it doesn't have to be a
  Mac, and it doesn't have to be *your* computer. A borrowed laptop is fine.
- ✅ **No jailbreak.**


> Full step-by-step (Mac / Windows / Linux): **[pairing guide](PAIRING-WINDOWS.md)** (uses idevice_pair in RPPairing mode).
>
> ⚠️ It has to be an **RPPairing** file. A `.mobiledevicepairing` you already
> have from SideStore or StikDebug is the older *lockdown* format — Mirage will
> tell you if you pick the wrong one.

### Steps
1. On a computer, get [idevice_pair](https://github.com/jkcoxson/idevice_pair/releases)
   (Mac / Windows / Linux). Windows also needs iTunes for the drivers.
2. Connect your iPhone by USB. **Unlock it**, tap **Trust**, and enter your
   passcode.
3. In idevice_pair pick **RPPairing** mode and **Generate** the file.
4. Send it to your iPhone — AirDrop, iCloud Drive, or email.
5. **Tap the file → "Open in Mirage"** (or Settings → Developer login → Import).

That's it — reusable forever, no computer needed again.

> Each iPhone needs its own pairing file (generated with that device plugged
> in), but only once per device.

## Using it on mobile data (5G / LTE)

**You do not need Wi-Fi.** Older versions of this page said you had to start a
teleport on Wi-Fi or a hotspot — that is no longer true, and Mirage no longer
asks you to go and find one.

What the location service actually needs is a route to the tunnel it connects
through. How that plays out depends on which tunnel you use:

### With Mirage's own VPN (paid signing)
Nothing to do. Mirage starts its own tunnel on cellular and teleports straight
away.

### With LocalDevVPN (free sideload)
Cellular and the tunnel can both be up and the connect still gets refused — with
mobile data as your only IPv4 route, nothing Mirage can do from inside the app
changes that. So:

1. Tap **Teleport**. Mirage sees the situation and asks for Mobile Data off.
2. Turn **Mobile Data off** — Settings, or Control Centre. You are not being
   asked to find Wi-Fi; you're taking cellular away for a few seconds.
3. Mirage notices the moment the route frees up and starts **by itself**. You do
   not have to tap anything again; it remembered where you were going.
4. Turn **Mobile Data back on**. The session keeps running.

That's one toggle per session, not per teleport — once a session exists,
teleporting somewhere else needs no route at all.

> If you have Wi-Fi available, none of this applies: connect and teleport
> normally. Wi-Fi alongside cellular works fine.

### Once it's running
- Change spots, use the joystick, follow a route — all on cellular.
- Stopping a spoof leaves the tunnel up, so starting again is quick.
- If a session does drop, Mirage re-applies it on its own.

## Keep a copy of your pairing file

From 3.1, every pairing file you import is also saved to
**Files → On My iPhone → Mirage → Pairing**, and **Settings → Developer login →
Save pairing file** can share it off the phone (AirDrop, iCloud Drive, wherever).

Do that once. If you ever reinstall Mirage, drop the file back into that folder
and it gets picked up automatically — no re-pairing, no computer.
