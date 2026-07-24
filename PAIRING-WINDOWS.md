# Make a pairing file on Windows (for Mirage)

Mirage's GPS override needs a **one-time pairing file** per iPhone. On iOS 17.4+
(incl. iOS 26/27) it must be an **RPPairing** file — use **idevice_pair**, not
the old jitterbugpair (that makes the wrong "Lockdown" format).

You only do this **once per iPhone**; the file is reusable afterwards.

## What you need
- A **Windows PC** (any — it doesn't have to be yours).
- **iTunes** installed from [apple.com](https://www.apple.com/itunes/download/win64)
  — this installs the USB drivers Windows needs to see the iPhone. Leave it
  installed.
- **idevice_pair** for Windows: download `iDevicePair--windows-x86_64.exe` from
  the [releases page](https://github.com/jkcoxson/idevice_pair/releases).
- A USB cable.

## Steps
1. Install iTunes, then reboot if it asks.
2. Plug the iPhone into the PC with the cable. **Unlock the phone**, and on the
   "Trust This Computer?" prompt tap **Trust** and enter your passcode.
3. Run **iDevicePair--windows-x86_64.exe**.
4. Pick your device, set mode to **RPPairing** (for iOS 17.4+), then click
   **Generate**. Tap **Trust** again on the phone if asked.
5. It saves a pairing file (e.g. `<UDID>.plist` / `.mobiledevicepairing`).

## Get it onto the iPhone
Send the file to the phone however's easiest — email it to yourself, or drop it
in iCloud Drive / Google Drive / OneDrive and open it there. Then:

**Mirage → Settings → Developer login → import the pairing file.**

Done. GPS override now works. (For sideloaded installs without the paid Network
Extension entitlement, also keep **LocalDevVPN** running — it provides the
loopback tunnel Mirage connects through.)

## Notes
- **One time per device**, reusable forever. Each new iPhone needs its own file
  (generated with that phone plugged in).
- No Mac and no jailbreak required. Mac/Linux users can use the same
  idevice_pair app in RPPairing mode.
