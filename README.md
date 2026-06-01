# NexusControl

The desktop companion app for the **[ЯHP]** alliance.

NexusControl is a single, self-contained Windows application. There is **no installer**, it needs **no administrator rights**, and it bundles everything it requires. You download one file, put it in a folder of your choice, and run it — the app creates everything else by itself on first launch.

---

## Requirements

- **Windows 10 or 11, 64-bit.**
- An **internet connection**.
- A **Discord account** that is a member of the **[ЯHP]** server (your visible content depends on your Discord roles).
- No .NET installation required — the runtime is included in the executable.

---

## Installation

1. **Download** the latest `NexusControl.exe` from the **Releases** page of the project.
2. **Create a folder** for the app in a location you can write to, for example:
   - `C:\Tools\NexusControl`  or  `D:\NexusControl`
   - Avoid `C:\Program Files\…` — that location is write-protected and the app needs to create its own files next to the executable.
3. **Move** `NexusControl.exe` into that folder.
4. **Start** the app with a double-click.

That's it. On the **first start** NexusControl automatically creates a `data` subfolder next to the executable and fills it with everything it needs (settings, logs, etc.). You do not have to configure anything.

```
NexusControl\
├─ NexusControl.exe      ← the app (the only file you download)
└─ data\                 ← created automatically on first launch
   ├─ config.json
   ├─ logs\
   └─ … (further files the app manages itself)
```

> **Windows SmartScreen warning on first start.**
> Because the app is not signed with a (paid) code-signing certificate, Windows may show *"Windows protected your PC"*. This is expected.
> Click **More info → Run anyway** once. Windows remembers your choice for this file.

---

## First start & sign-in

1. After launch, click **"Sign in with Discord"**.
2. Authorize the app in your browser.
3. You're in. Which tabs and data you see depends on your Discord roles in the **[ЯHP]** server.

Your login is stored encrypted in `data\` and is tied to your Windows user account — it cannot simply be copied to another PC or user.

---

## Updates

NexusControl **checks for a newer version automatically every time it starts**. If one is available, it asks you whether to update; on confirmation it downloads the new version, replaces itself, and restarts. You don't need to download anything manually.

If you ever want to update by hand, simply download the newest `NexusControl.exe` from the Releases page and overwrite the old one in your folder. Your `data` folder stays untouched.

---

## Moving or backing up

The app is fully **portable**. To move it to another folder or drive, just move the whole `NexusControl` folder (the `.exe` **and** the `data` folder) together. To back up your settings, copy the `data` folder.

> Note: the encrypted login token is bound to your Windows user. On a **different PC or Windows account** you will simply be asked to sign in again — everything else works.

---

## Uninstalling

There is nothing to uninstall. **Delete the `NexusControl` folder** and the app is gone, including all of its data.

---

## Troubleshooting

- **"Windows protected your PC" (SmartScreen):** click *More info → Run anyway*. See above.
- **Antivirus flags the file:** self-contained, unsigned single-file apps are occasionally false-flagged. Download only from the official Releases page; if needed, add an exception for the folder.
- **App won't create its files / errors on start:** make sure the folder is **writable** (not `Program Files`, not a read-only/blocked location). Move the folder to e.g. `C:\Tools\NexusControl` and try again.
- **No data / tabs missing after sign-in:** this is normal if your Discord roles don't grant access — check your roles in the **[ЯHP]** server.
- **Need to reset:** close the app and delete the `data` folder. It will be recreated cleanly on the next start (you'll need to sign in again).
- **Logs** for support live in `data\logs\`.

---

*NexusControl is an internal tool for the [ЯHP] alliance. Please don't redistribute the executable outside the alliance.*
