# Hara-One Desktop — releases

Installers and updates for **Hara-One Desktop**, the Hara-One app for Windows and macOS. This
repository holds releases only; the app's source is private.

## Which release is yours

Each company has its own app. Releases are tagged `haraone-<company>-v<version>`. Download
from your company's latest release:

| Company | Tag |
|---|---|
| Debi Corporation | `haraone-debi-v…` |

Your installed app checks this page for new versions on its own. It also checks when you
choose **Settings → Updates → Check now**.

## Installing

- **Windows:** download the `…_x64-setup.exe` file and run it.
  - It installs for your user only and needs no administrator rights.
  - If Windows says "Windows protected your PC", choose **More info → Run anyway**.
- **Mac:** download the `…_universal.dmg` file, open it, and drag Hara-One to Applications.
  - It runs on Apple silicon and Intel Macs, macOS 13.3 or newer.
  - If macOS blocks the first launch, open **System Settings → Privacy & Security → Open Anyway**.

## Checking a download

Every installer comes with a `.sha256` file holding its SHA-256 checksum. The app checks
updates against it before it installs anything.

To check a download by hand:

```sh
# Windows (PowerShell)
Get-FileHash .\<installer> -Algorithm SHA256
# macOS
shasum -a 256 <installer>
```

You sign in with your usual Hara-One account. The app holds no passwords or keys of its own,
and your company's Hara-One permissions decide what you can see.
