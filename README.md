# ImagineXI

**ImagineXI** is a free, community-hosted FINAL FANTASY XI private server and research project.

This repository hosts the launcher download and the rolling update channel the launcher pulls from.

## Download

Everything we ship is listed below â€” no hidden bundle. You can **browse every support file** in [`dist/`](https://github.com/markup-ux/imaginexi-updates/tree/main/dist) on GitHub before downloading anything.

From the **[live release page](https://github.com/markup-ux/imaginexi-updates/releases/tag/live)**, download these four files into the **same folder**:

1. **[ImagineXILauncher.exe](https://github.com/markup-ux/imaginexi-updates/releases/download/live/ImagineXILauncher.exe)** â€” the launcher program (.NET 9, self-contained)
2. **[launcher_config.json](https://github.com/markup-ux/imaginexi-updates/releases/download/live/launcher_config.json)** â€” default launcher settings
3. **[launcher_manifest.json](https://github.com/markup-ux/imaginexi-updates/releases/download/live/launcher_manifest.json)** â€” package list used by Install / Update
4. **[launcher-assets.zip](https://github.com/markup-ux/imaginexi-updates/releases/download/live/launcher-assets.zip)** â€” support files; **extract in the same folder** as the `.exe`

Then run `ImagineXILauncher.exe`.

The launcher installs and updates everything ImagineXI-specific automatically (loader, Windower bundle, overlay, addons). Updates are picked up every time you start the launcher.

### Why not one zip?

We publish separate files so you can inspect each download on GitHub, verify checksums (below), and see exactly what each file does before running anything. Windows may still warn about an unsigned `.exe` â€” that is normal for indie software; checksums let you confirm you got the real file.

## What's in the download?

| File / folder | What it is |
|---------------|------------|
| `ImagineXILauncher.exe` | ImagineXI WPF launcher (our code). Connects to the server, installs updates, launches Windower/xiloader. |
| `launcher_config.json` | Points the launcher at the update manifest and optional UI paths. |
| `launcher_manifest.json` | Lists package zips the launcher downloads on Install / Update. |
| `Assets/blkmoogle.png` | Launcher UI artwork. |
| `Assets/README.txt` | Notes about launcher art/audio paths. |
| `Assets/Tools/vgmstream/*` | [vgmstream](https://github.com/vgmstream/vgmstream) audio decoder (open source). Used only if you enable optional theme music and have a retail FFXI install configured â€” it reads *your* game audio locally; nothing is uploaded. |
| `Assets/VisualEnhancement/dgVoodoo.conf` | Optional dgVoodoo wrapper config for HD visuals. |
| `Fonts/OFL-Cinzel.txt` | SIL Open Font License for the Cinzel UI font (embedded in the `.exe`). |

We **do not** ship Square Enix game files, keyloggers, miners, or remote-access tools. [`LAUNCHER_MANIFEST.json`](LAUNCHER_MANIFEST.json) lists every support file with SHA256 hashes.

## Verify downloads (SHA256)

<!--LAUNCHER_PUBLISHED_START-->
Last launcher publish: pending first publish.
<!--LAUNCHER_PUBLISHED_END-->

<!--LAUNCHER_CHECKSUMS_START-->
Checksum table is refreshed automatically when we publish a new launcher build.
<!--LAUNCHER_CHECKSUMS_END-->

PowerShell verification example:

```powershell
Get-FileHash .\ImagineXILauncher.exe -Algorithm SHA256
Get-FileHash .\launcher-assets.zip -Algorithm SHA256
```

## You need the official FFXI client (and why)

ImagineXI **does not distribute any of Square Enix's copyrighted game files.** You install the official FINAL FANTASY XI client yourself, and the launcher uses that installation.

Why:

- FINAL FANTASY XI's client, art, music, and data belong to Square Enix. Redistributing them is copyright infringement.
- ImagineXI is run as a **research project**, and we want it to be as legally sound as possible. Everything we distribute is our own work or properly licensed open-source software â€” never Square Enix's assets.

The official client is a free download from Square Enix's own servers. You do not need a registration code, a PlayOnline account, or a subscription to play on ImagineXI â€” those are only required for Square Enix's official retail service.

## Installing the official FFXI client

1. Go to Square Enix's official download page:
   - **Americas / Global:** https://www.playonline.com/ff11us/download/media/install_win.html
   - **Europe:** https://www.playonline.com/ff11eu/download/media/install_win.html
2. Download **all five parts** (`FFXIFullSetup_US.part1.exe` + four `.rar` parts, ~7 GB total) into the **same folder**.
3. Run `FFXIFullSetup_US.part1.exe` and click **Extract**. Note the output folder it creates (`FFXIFullSetup_US`).
4. Inside that folder, run **`FFXISetup.exe`**, check every component (PlayOnline Viewer, FINAL FANTASY XI, expansions), and click **Install**.
5. When the installer finishes, you're done â€” **do not** launch PlayOnline or pay for anything. ImagineXI's launcher takes it from here.

> Community walkthrough with screenshots: [BG-Wiki Install Guide](https://www.bg-wiki.com/ffxi/Install_Guide) (follow only the *download and install* part â€” account setup and version update are **not** needed for ImagineXI).

## Setting up ImagineXI

1. Run `ImagineXILauncher.exe`.
2. Press **Install / Update** and let it finish.
3. In **Settings**, point **Retail POL executable** at your FFXI installation (usually `C:\Program Files (x86)\PlayOnline\SquareEnix\PlayOnlineViewer\pol.exe`) and press **Save**.
4. Back on **Home**, press **Create Account**, then **Play** â€” you'll land at character select.

Questions or problems? Join the Discord (button in the launcher).

## Connecting with your own setup

Already have FFXI and your own private-server loader configured? You only need the server address:

<!--SERVER_ADDRESS_START-->
```
24.148.24.152
```

For example, with xiloader: `xiloader.exe --server 24.148.24.152 --user youraccount`
<!--SERVER_ADDRESS_END-->

This address can change from time to time. The address above is refreshed automatically with every update we publish, and the always-current value is also in the [launcher manifest](https://github.com/markup-ux/imaginexi-updates/releases/download/live/launcher_manifest.json) (`ServerAddress` field). The launcher handles this for you automatically.

## Legal

ImagineXI is a non-commercial research project. It is not affiliated with or endorsed by Square Enix. FINAL FANTASY is a registered trademark of Square Enix Holdings Co., Ltd. All game assets remain the property of their respective owners; this project distributes none of them.
