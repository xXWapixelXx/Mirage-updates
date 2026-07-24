# Mirage — first-time setup

Mirage installs like any sideloaded app, then needs **one** small setup step so
it can override GPS.

## 1. Install the app
Mirage is invite-only — see the [README](README.md) to get access. Install it
with your sideloading tool of choice (SideStore / AltStore, or a signed build).
EU users can install with **AltStore PAL** straight from Safari, no computer.

## 2. One-time pairing (needed for GPS spoofing)
To set your GPS location, iOS requires a **one-time trust** ("pairing") between
your iPhone and a computer. This is an Apple security step — it can't be done on
the phone alone. The good news:

- ✅ **One time only** — the pairing file is reusable forever after.
- ✅ **Any computer** works (Windows, macOS, or Linux) — it doesn't have to be a
  Mac, and it doesn't have to be *your* computer. A borrowed laptop is fine.
- ✅ **No jailbreak.**


> Full step-by-step (Mac / Windows / Linux): **[pairing guide](PAIRING-WINDOWS.md)** (uses idevice_pair in RPPairing mode).

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

iOS only lets the location service **start** over Wi-Fi / hotspot / USB (Apple
blocks the *initial* connection on cellular). But once it's running:

- **Start a teleport on Wi-Fi or a hotspot** (one moment is enough).
- **Then it keeps working on 5G** — change spots, use the joystick, all on
  cellular — as long as you stay spoofing.
- Turn it off, force-close, or lose the session and you'll need Wi-Fi to start
  again. Mirage **auto-reconnects** the moment Wi-Fi is back.
