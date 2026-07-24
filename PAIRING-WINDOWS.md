# Make a pairing file — Mac / Windows / Linux

Mirage's GPS override needs a **one-time pairing file** per iPhone. On iOS 17.4+
(incl. iOS 26/27) it must be an **RPPairing** file — use **idevice_pair**, not
the old jitterbugpair (that makes the wrong "Lockdown" format).

You do this **once per iPhone** on any computer; the file is reusable forever and
works across your other tools (StikDebug, SideStore) too.

## What you need
- Any computer — **Mac, Windows, or Linux** (it doesn't have to be yours).
- **idevice_pair** for your OS — download from the
  [releases page](https://github.com/jkcoxson/idevice_pair/releases).
- A USB cable.
- **Windows only:** install **iTunes** from
  [apple.com](https://www.apple.com/itunes/download/win64) for the USB drivers.
  **Mac & Linux need no extra drivers** (macOS has them built in; on Linux make
  sure `usbmuxd` is running).

## Steps (same on every OS)
1. Plug the iPhone into the computer with the cable. **Unlock the phone** and tap
   **Trust** + enter your passcode.
2. Open **idevice_pair**, pick your device.
3. Set mode to **RPPairing** (for iOS 17.4+), then click **Generate**. Tap
   **Trust** again on the phone if asked.
4. It saves a pairing file (e.g. `<UDID>.plist` / `.mobiledevicepairing`).

## Get it onto the iPhone
Send the file to the phone — **AirDrop** (Mac), email, or iCloud / Google Drive /
OneDrive. Then just **tap the file → "Open in Mirage"** — it imports instantly.
(Or in the app: **Settings → Developer login → Import pairing file**.)

Done — GPS override works, and keeps working on 5G once started.

## Notes
- **One time per device**, reusable forever. Each new iPhone needs its own file.
- No jailbreak, no Mac required (any computer works, once).
- For sideloaded installs without the paid Network-Extension entitlement, keep
  **LocalDevVPN** running — it provides the loopback tunnel Mirage connects through.
