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

iOS only lets the location service **start** over Wi-Fi / hotspot / USB (Apple
blocks the *initial* connection on cellular). But once it's running:

- **Start a teleport on Wi-Fi or a hotspot** (one moment is enough).
- **Then it keeps working on 5G** — change spots, use the joystick, all on
  cellular — as long as you stay spoofing.
- Turn it off, force-close, or lose the session and you'll need Wi-Fi to start
  again. Mirage **auto-reconnects** the moment Wi-Fi is back.
