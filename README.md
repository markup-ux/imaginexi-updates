# ImagineXI

**ImagineXI** is a free, community-hosted FINAL FANTASY XI private server and research project.

This repository hosts the launcher download and the rolling update channel the launcher pulls from.

## Download

<!--LAUNCHER_DOWNLOAD_START-->
Pick whichever you prefer from the **[live release page](https://github.com/markup-ux/imaginexi-updates/releases/tag/live)**:

### Quick download (one zip)

**[ImagineXILauncher.zip](https://github.com/markup-ux/imaginexi-updates/releases/download/live/ImagineXILauncher.zip)** - extract anywhere and run `ImagineXILauncher.exe`.

Same contents as the separate files below, packaged for convenience.

### Inspect before you run (separate files)

Everything we ship is listed here - no hidden bundle. You can **browse every support file** in [`dist/`](https://github.com/markup-ux/imaginexi-updates/tree/main/dist) on GitHub before downloading anything.

Download these four files into the **same folder**:

1. **[ImagineXILauncher.exe](https://github.com/markup-ux/imaginexi-updates/releases/download/live/ImagineXILauncher.exe)** - the launcher program (.NET 9, self-contained)
2. **[launcher_config.json](https://github.com/markup-ux/imaginexi-updates/releases/download/live/launcher_config.json)** - default launcher settings
3. **[launcher_manifest.json](https://github.com/markup-ux/imaginexi-updates/releases/download/live/launcher_manifest.json)** - package list used by Install / Update
4. **[launcher-assets.zip](https://github.com/markup-ux/imaginexi-updates/releases/download/live/launcher-assets.zip)** - support files; **extract in the same folder** as the `.exe`

Then run `ImagineXILauncher.exe`.

The launcher installs and updates everything ImagineXI-specific automatically (loader, Windower bundle, overlay, addons). Updates are picked up every time you start the launcher.

### About Windows security warnings

Windows may warn about an unsigned `.exe` - that is normal for indie software. Use the SHA256 checksums below to confirm you got the real files, or browse [`dist/`](https://github.com/markup-ux/imaginexi-updates/tree/main/dist) before downloading.
<!--LAUNCHER_DOWNLOAD_END-->

## What's in the download?

| File / folder | What it is |
|---------------|------------|
| `ImagineXILauncher.zip` | Full launcher bundle (exe, configs, Assets/, Fonts/). Extract and run. |
| `ImagineXILauncher.exe` | ImagineXI WPF launcher (our code). Connects to the server, installs updates, launches Windower/xiloader. |
| `launcher_config.json` | Points the launcher at the update manifest and optional UI paths. |
| `launcher_manifest.json` | Lists package zips the launcher downloads on Install / Update. |
| `Assets/blkmoogle.png` | Launcher UI artwork. |
| `Assets/README.txt` | Notes about launcher art/audio paths. |
| `Assets/Tools/vgmstream/*` | [vgmstream](https://github.com/vgmstream/vgmstream) audio decoder (open source). Used only if you enable optional theme music and have a retail FFXI install configured  - it reads *your* game audio locally; nothing is uploaded. |
| `Assets/VisualEnhancement/dgVoodoo.conf` | Optional dgVoodoo wrapper config for HD visuals. |
| `Fonts/OFL-Cinzel.txt` | SIL Open Font License for the Cinzel UI font (embedded in the `.exe`). |

We **do not** ship Square Enix game files, keyloggers, miners, or remote-access tools. [`LAUNCHER_MANIFEST.json`](LAUNCHER_MANIFEST.json) lists every support file with SHA256 hashes.

## Verify downloads (SHA256)

<!--LAUNCHER_PUBLISHED_START-->
Last launcher publish: **2026-06-11 08:09** (UTC). Re-run `Get-FileHash` on your downloads to match the table below.
<!--LAUNCHER_PUBLISHED_END-->

<!--LAUNCHER_CHECKSUMS_START-->
| File | SHA256 | Size |
|------|--------|------|
| `ImagineXILauncher.zip` | `DB1A731DDF7624071088979FB7A518D807C02A4FD19F34342EA8A8BFD7896743` | 78.4 MB |
| `ImagineXILauncher.exe` | `E73D491DF0329F0212A6C6060009C026FBEC5646776B08F4228A91DCB8D4801B` | 170.1 MB |
| `launcher_config.json` | `A01A5AE29A483CE3B0B78A9BE1D0E0D96E7B977FA99A7B174F81EE7733BAB429` | 471 B |
| `launcher_manifest.json` | `5430DD38AED243950F1F31509133DF8AAA15CADFC603C28E7BD65D8F71BF7AD3` | 8 KB |
| `launcher-assets.zip` | `A393AE1C7C0609B20C1A7E479AEB6B9EB7B359458AD439FB3D91AE723B9F3BF6` | 6.1 MB |

<details>
<summary>All support files inside <code>launcher-assets.zip</code></summary>

| Path | SHA256 | Size |
|------|--------|------|
| `Assets/blkmoogle.png` | `D314CF3EE4AFC9AF41167D6694628A4CA3FC5F877E6905C180FAEE17CC9BB7DD` | 2.0 MB |
| `Assets/README.txt` | `330AC3D7B2DF7A25C28B1266EF1A4F4CFC574D267AB97B890769A232B0A26E43` | 1 KB |
| `Assets/Tools/vgmstream/avcodec-vgmstream-59.dll` | `4D6CF54E7B3C26EF06E95BDB515A10D1E1BED3EC1FFD87EC3E5C4FBCD2A883F6` | 2.3 MB |
| `Assets/Tools/vgmstream/avformat-vgmstream-59.dll` | `0DDE66EA268CCCB67B1AA219C1CE879602B839E561A79A00C8215E2688F1A4B2` | 1.2 MB |
| `Assets/Tools/vgmstream/avutil-vgmstream-57.dll` | `A999856C17CFDCE3C22B92B6640A7ADA6C4AB4C3C6841A863770B72FA0BC19B4` | 1.7 MB |
| `Assets/Tools/vgmstream/COPYING` | `FCC26D35C4C4365E31F21734F846E4EE362FF0B57BA696085605A7B4768D8763` | 1 KB |
| `Assets/Tools/vgmstream/libatrac9.dll` | `FE82F1AE13A798337E03942C35351997C23CAADB5EB0C6B7A2DC2A521ED8B02E` | 302 KB |
| `Assets/Tools/vgmstream/libcelt-0061.dll` | `542254723D9100F91CBF18E41C4AFF80287C22A9859E9E545C413D984DF440AD` | 108 KB |
| `Assets/Tools/vgmstream/libcelt-0110.dll` | `BFCC51D865BB3B6A2793381BF535F23EC423FEB722B46333FA8556CCDCAFA61A` | 103 KB |
| `Assets/Tools/vgmstream/libg719_decode.dll` | `AAD61F205CE1F1B61285F6B37B90A331EC8C6AE2F94F361714DC21A12C236960` | 153 KB |
| `Assets/Tools/vgmstream/libmpg123-0.dll` | `DB9EB1D91B8EB9F47B0968201DBF6C51A9627E539A78AFD9AD5F59C5D18FE4DF` | 410 KB |
| `Assets/Tools/vgmstream/libspeex-1.dll` | `04DBC85FCEC6C54671535BF39937A70F2DD040A81AD670A0B84DE6CA17B39BFF` | 127 KB |
| `Assets/Tools/vgmstream/libvorbis.dll` | `5F330A20B19B3C70DC43EEDCC95891E65940FCA04A77155C573EFCDD4C2CA665` | 281 KB |
| `Assets/Tools/vgmstream/swresample-vgmstream-4.dll` | `688A81D31EF98A9A6143E1075B2F4C5B79BDFA51E7A14D50D662A0E916DAC739` | 713 KB |
| `Assets/Tools/vgmstream/vgmstream-cli.exe` | `29DF08C557ADA8269C92A6ABFE3886AD2F65849B0B26BA78A0819B363BBC5B85` | 2.7 MB |
| `Assets/VisualEnhancement/dgVoodoo.conf` | `A1EBA8842DC7043018FBE18D2B2390265D509563A7765EC904ECF9C735C47618` | 374 B |
| `Fonts/OFL-Cinzel.txt` | `F2B3029ABA64C378BF0963B62945EEE15E564FE4330B934C8F2EB058282B5E83` | 4 KB |

</details>
<!--LAUNCHER_CHECKSUMS_END-->

PowerShell verification example:

```powershell
Get-FileHash .\ImagineXILauncher.zip -Algorithm SHA256
Get-FileHash .\ImagineXILauncher.exe -Algorithm SHA256
Get-FileHash .\launcher-assets.zip -Algorithm SHA256
```

## You need the official FFXI client (and why)

ImagineXI **does not distribute any of Square Enix's copyrighted game files.** You install the official FINAL FANTASY XI client yourself, and the launcher uses that installation.

Why:

- FINAL FANTASY XI's client, art, music, and data belong to Square Enix. Redistributing them is copyright infringement.
- ImagineXI is run as a **research project**, and we want it to be as legally sound as possible. Everything we distribute is our own work or properly licensed open-source software  - never Square Enix's assets.

The official client is a free download from Square Enix's own servers. You do not need a registration code, a PlayOnline account, or a subscription to play on ImagineXI  - those are only required for Square Enix's official retail service.

## Installing the official FFXI client

1. Go to Square Enix's official download page:
   - **Americas / Global:** https://www.playonline.com/ff11us/download/media/install_win.html
   - **Europe:** https://www.playonline.com/ff11eu/download/media/install_win.html
2. Download **all five parts** (`FFXIFullSetup_US.part1.exe` + four `.rar` parts, ~7 GB total) into the **same folder**.
3. Run `FFXIFullSetup_US.part1.exe` and click **Extract**. Note the output folder it creates (`FFXIFullSetup_US`).
4. Inside that folder, run **`FFXISetup.exe`**, check every component (PlayOnline Viewer, FINAL FANTASY XI, expansions), and click **Install**.
5. When the installer finishes, you're done  - **do not** launch PlayOnline or pay for anything. ImagineXI's launcher takes it from here.

> Community walkthrough with screenshots: [BG-Wiki Install Guide](https://www.bg-wiki.com/ffxi/Install_Guide) (follow only the *download and install* part  - account setup and version update are **not** needed for ImagineXI).

## Setting up ImagineXI

1. Run `ImagineXILauncher.exe`.
2. Press **Install / Update** and let it finish.
3. In **Settings**, point **Retail POL executable** at your FFXI installation (usually `C:\Program Files (x86)\PlayOnline\SquareEnix\PlayOnlineViewer\pol.exe`) and press **Save**.
4. Back on **Home**, press **Create Account**, then **Play**  - you'll land at character select.

Questions or problems? Join the Discord (button in the launcher).

## Connecting with your own setup

Already have FFXI and your own private-server loader configured? You only need the server address:

<!--SERVER_ADDRESS_START-->
```
172.56.17.95
```

For example, with xiloader: `xiloader.exe --server 172.56.17.95 --user youraccount`
<!--SERVER_ADDRESS_END-->

This address can change from time to time. The address above is refreshed automatically with every update we publish, and the always-current value is also in the [launcher manifest](https://github.com/markup-ux/imaginexi-updates/releases/download/live/launcher_manifest.json) (`ServerAddress` field). The launcher handles this for you automatically.

## Legal

ImagineXI is a non-commercial research project. It is not affiliated with or endorsed by Square Enix. FINAL FANTASY is a registered trademark of Square Enix Holdings Co., Ltd. All game assets remain the property of their respective owners; this project distributes none of them.
