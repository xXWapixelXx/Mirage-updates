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

### Steps
1. On a computer, get a pairing tool — e.g. [idevice_pair](https://github.com/jkcoxson/idevice_pair)
   (Windows/macOS/Linux) or JitterbugPair.
2. Connect your iPhone by USB. **Unlock it**, tap **Trust**, and enter your
   passcode.
3. Generate the pairing file (a `.mobiledevicepairing` / `.plist` file).
4. Send that file to your iPhone — AirDrop, iCloud Drive, or email.
5. Open **Mirage → Settings → import the pairing file.**

That's it. From now on Mirage spoofs on-device with no computer needed.

> Each iPhone needs its own pairing file (generated with that device plugged
> in), but only once per device.
