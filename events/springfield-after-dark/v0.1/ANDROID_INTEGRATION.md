# Android client inspection: Event 001 integration

Inspection date: 2026-10-25

## Files inspected

- User-provided `BluSpringfield-Offline-Test-unsigned(1).apk`, **76,447,219 bytes**
- Earlier user-provided `assets.zip` (**25,202,407 bytes**), with its contents compared against the APK

## Verified findings

1. Android manifest identifies package `com.ea.game.simpsons4_row.Springfield`, version code **695**, version name **4.70.5**, minimum SDK 21 and target SDK 34.
2. The game engine is primarily native, under `lib/<abi>/libscorpio.so`. Both `classes.dex` and `classes2.dex` are present.
3. APK has **713 ZIP entries**, including **26 entries under `assets/`**. The supplied older `assets.zip` includes the same **26 files byte-for-byte**, not the downloaded game data.
4. Built-in `assets/core/res-core/1` is a ZIP containing fonts, UI XML and language files, rather than the actual Springfield building/quest data.
5. Native engine strings reference separate content indexes and databases, including `DLCIndex-v4-69-5-412AA04C483EBCA5.xml`, `QuestPackages.xml`, `SpecialEventList.xml`, `GameObjectBundlesMasterList.xml`, `BuildingMasterList.xml`, `CharacterMasterList.xml`, and `JobMasterList.xml`. Those game data/XML files are **not present** in the supplied APK or `assets.zip`.
6. The uploaded APK is **unsigned**: no v1 certificate files and no APK Signing Block magic. It cannot replace a previously signed version while retaining its app data unless re-signed with the **same certificate/key** as the installed app.
7. **SHA-256 (uploaded APK):** `8182be2fdc2ddcf9ca4915601fe13a17a74823675a88e016212a1b71df2ebcd4`

## What this means for Springfield After Dark

The JSON event model and browser prototype in this branch are **not directly understood by the native Scorpio game engine**. Packaging those files inside an APK without the appropriate content-loader definitions would **not make the event appear** and would risk introducing an unusable build. The native game also needs appropriate sprite/animation bundles.

This branch does **not** include a patched APK. No claims of successful native integration or game launch testing are made.

## Missing inputs for genuine integration

- The game's **downloaded content/cache packs** from the actual working offline build; they are not part of the APK.
- Current native **event, quest, building, character, job and prize definitions**, in the engine's real format, or a source project with a supported content loader.
- Art/sprite bundle pipeline or compatible existing game asset-format examples.
- The signing keystore **already used** to sign the installed app, if this build must update over it without losing progress.
- A running Android test device/emulator to verify loading, saves, quest progression and crash-free install.

## How to locate data on a connected Android device

First inspect possible external app-data locations, without deleting or changing anything:

```sh
adb shell 'ls -la /sdcard/Android/data/com.ea.game.simpsons4_row.Springfield/'
adb shell 'ls -la /sdcard/Android/obb/com.ea.game.simpsons4_row.Springfield/'
```

These paths are **candidates**, not confirmed. Some versions use Android-private or other directories and may not expose cached files through ADB without root or a debug build.

If found, copy only the game's externally accessible downloaded data from the device and inspect its format before any modifications. Keep original backups and installed save data intact.

## Integration checklist

- Map `event.json` and `quests.json` to the native XML/object definitions.
- Register event in actual `SpecialEventList.xml` / content indices.
- Integrate item and job IDs with native master lists and add real approved sprite bundles.
- Handle unlocks, progress persistence, daily limits, timing and event expiry.
- Test device rendering and saves; verify an update with the original signing key.
- Do not claim success until the modified app visibly loads the new event in the actual Springfield town.
