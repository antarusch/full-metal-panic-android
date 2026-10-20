# Alpha 71 master + Alpha 72 branding update

## Downloads in this release

- **Alpha 71 protected master:** `Full_Metal_Panic_Android_Alpha71_MASTER.apk` — the exact preserved master APK.
- **Alpha 72 IconFix branding update:** `Full_Metal_Panic_Android_Alpha72_IconFix.apk` — the newer app icon/background packaging, using the same signing identity. The original masters remain preserved.

Both are alpha snapshots. The branding update is supplied separately so the exact master remains available. Android only permits a normal update to a higher version code; install the master first if you intend to compare both builds.

SHA-256 values are in `SHA256SUMS.txt`. APK signatures and archive integrity were checked before preparing this release.

## What was changed for Full Metal Panic!

- Adapted the original runtime and Android launcher specifically for **Full Metal Panic! Fight! Who Dares Wins, PS4 CUSA09316 v1.00**, running x86-64 game code on ARM64 through FEXCore.
- Expanded PS4 compatibility for memory management, threading and synchronization, module loading, and the system-service calls required by the game and its Unity/Mono integration.
- Added support for loading and initializing required game-provided modules, including the game's dialog and saved-game paths, from the user's game files.
- Fixed texture-cache alias synchronization and image-resolution handling that caused black-screen rendering.
- Adapted controller polling and Android touchscreen controls, and added the offline service/trophy compatibility needed to continue into gameplay.

These changes are specific to this title. They do not establish compatibility with other PS4 games.

## Foundation and thanks

This is a **heavily modified, game-specific adaptation of the God of War III Android runtime**, originally developed in [zFitness/gow3_android](https://github.com/zFitness/gow3_android). It is configured to run only the game named in this project. It is not a general-purpose PS4 emulator and is not intended to run God of War III or other games.

A huge thank you to **zFitness and all owners, maintainers, and contributors of the God of War III Android runtime**. Without their work, these two adaptations would not have been possible. Their runtime, Android integration, and graphics foundation made this work possible. Please support and credit the original project.

Credit also remains with the upstream projects and contributors used by that runtime, including FEXCore, shadPS4, and its other dependencies. Original copyright and license notices remain applicable. The upstream runtime is GPL-2.0-or-later; third-party components retain their respective licenses. These adaptations are independent work and are not official releases from the upstream authors or the game publishers.

## AI development and testing limits

These projects were **made with AI (ChatGPT/Codex)**, with human-guided development and testing on an Android phone. AI was used to help develop compatibility changes, diagnose logs, modify runtime and graphics code, and build and package the APKs.

**Only the first levels have been tested.** The full games have not been completed or validated. There may be bugs, crashes, rendering problems, or freezes later in the game. These are experimental alpha releases.

## Game files and device

No game executable or proprietary game-data files are included in these APK downloads. Supply your own legally obtained files for the supported game/version.

Testing was performed on a REDMAGIC 10S Pro running Android 16, with a Snapdragon 8 Elite Leading Version, Adreno 830, and 24 GB RAM. Vulkan/Turnip graphics are used; Turnip Gen8 V37 is the preferred driver. Other devices and drivers are not comprehensively tested.
