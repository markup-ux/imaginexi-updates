# ImagineXI

**ImagineXI** is a free, community-hosted FINAL FANTASY XI private server.

This repository hosts the launcher download and the rolling update channel the launcher pulls from.

## Imagine XI 2.0

**[Download the Imagine XI 2.0 launcher](https://github.com/markup-ux/imaginexi-updates/releases/download/ixi20/ImagineXI20-Launcher.zip)** — unzip and run `ImagineXILauncher.exe`. Official FFXI client required (not included). Leave **Play on this PC** unchecked.

### Server

- Cap: main 75 / sub 37
- Start at level 1. No Limit Breaks. Level freely to 75.
- All jobs unlocked at creation (WAR–RUN). No Trusts.
- Subjob unlocked from the start.

### Progression

- Abilities, traits, and magic unlock by 37. Two-hours and one-hours from level 1; timed SPs last 2 minutes.
- Dual Wield V on WAR–RUN. Treasure Hunter 3 on THF / BST / RNG / COR.
- Casters get Refresh, Conserve MP, and Fast Cast. RDM Shield Mastery at 1.
- Native weapons A+. Ninjutsu A+ on every job. Songs A+ on BRD.
- Combat, magic, and defensive skills stay at your stored job cap.

### Economy & gear

- Gil and Sparks convert to XP. Shops do not sell weapons or armor. Remaining NPC / guild stock is free.
- All equipment is usable on all jobs.
- First time you play a job: one starter crate (need inventory space).
- Decent Challenge+ kills drop gear in any zone: starter / pantheon through 20, then shop-tier kits.
- Too Weak drops nothing. 10% cosmetic drop on EXP kills (including NMs).
- NM first-kill XP burst. Vendor sells of combat gear become XP.
- Exchange NPC next to conquest / signet guards (Sparks spend-only).
- Auction House is a gift locker — no gil fees or payouts.

### Combat & jobs

- Provoke on MNK / PLD / NIN / RUN.
- Infinite combat ammo (still equip legal ammo). Ninjutsu needs no tools.
- Instant Warp scrolls are not consumed. Teleports do not require a prior visit.
- Mana Wall is a toggle (3s recast to turn off).
- Cascade: 8 min, 10% MAB. SCH: 5×48s stratagems. Accession / Manifestation / Diffusion: 45s multi-spell windows.
- DRG wyvern is always hybrid DD + party support.
- NIN / SAM / DRG stances last 1 hour.
- Corsair: all Phantom Rolls from the start; Quick Draw needs no cards.
- Crafting: valid recipes never break; HQ stays retail; skill-ups are 4.5× more often.

### Quality of life

- On death, a spirit raises you (weakness stays). Skipped if Reraise is up.
- Spells auto-learned on login / level-up / job change.
- Discarded items become community caskets.
- Crag crystals + both airship passes on create/login. All maps and Survival Guides unlocked. Mounts at main level 10.
- Homepoints, airships, chocobos, and other travel fees are free.
- Half of gained XP also levels your current subjob (capped at 37).
- 80-slot inventory + full mog storage. Locker works in all areas with no expiry. Mog House 2F unlocked.
- Party Level Sync can raise or lower to the designee's stored main job.
- Refresh I and II stack on one effect (cap 9). Self/party enhancing, songs, and rolls last until zone, death, or job change.

### Launcher

- Theme music: Maginary originals. Skip, shuffle, and volume in the footer. Listen on opens the official stores.

### Client

- Isolated install folder. XIPivot DAT overlay for all-jobs gear.
- Does not patch retail ROM files.
- Overlay HUD — type `//ixo help` in game.

## This week in Vana'diel

Once people are playing, we post a weekly census of how the server looks: most-used jobs, common parties, food, and spells. Public totals, no character names. Same idea as retail’s old chalkboard.

Full chalkboard: [CENSUS.md](CENSUS.md)

## You need the official FFXI client (and why)

ImagineXI **does not distribute any of Square Enix's copyrighted game files.** You install the official FINAL FANTASY XI client yourself, and the launcher uses that installation.

Why:

- FINAL FANTASY XI's client, art, music, and data belong to Square Enix. Redistributing them is copyright infringement.
- Everything we distribute is our own work or properly licensed open-source software — never Square Enix's assets.

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
24.148.24.152
```

For example, with xiloader: `xiloader.exe --server 24.148.24.152 --user youraccount`
<!--SERVER_ADDRESS_END-->

This address can change from time to time. The address above is refreshed automatically with every update we publish, and the always-current value is also in the [launcher manifest](https://github.com/markup-ux/imaginexi-updates/releases/download/ixi20/launcher_manifest.json) (`ServerAddress` field). The launcher handles this for you automatically.

## Legal

ImagineXI is a non-commercial fan server. It is not affiliated with or endorsed by Square Enix. FINAL FANTASY is a registered trademark of Square Enix Holdings Co., Ltd. All game assets remain the property of their respective owners; this project distributes none of them.
