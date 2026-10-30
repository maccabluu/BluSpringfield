# Haunted Cottage animation tester v0.3

## Test file

Conversation deliverable: `BluSpringfield_Scooby_House_Animation_Tester_v0.3.html`, with bundled ZIP `BluSpringfield_Scooby_House_Animation_Tester_v0.3.zip`.

This is a standalone offline HTML file using the **exact previously approved haunted cottage PNG** embedded in the file, not a newly generated image.

## Implemented in the browser preview

- Chimney smoke movement, window light flicker, pumpkin light pulse.
- Day/night switch, individual effect toggles, animation pause.
- Haunted house click reaction with a floating candy reward.
- Add new house to an empty plot, move it, keep original cottage slot fixed.
- Candy and clues and state save attempt to browser localStorage.
- Four actual Homer APK sound effects, extracted from the user-supplied `BluSpringfield-Offline-Test-unsigned(1).apk` and transcoded to MP3 for the offline browser preview:
  - `103_drop_building.wav`: place
  - `05_reward_collect.wav`: reward
  - `08_confirm_bldng.wav`: confirm
  - `09_cancel_bldng.wav`: cancel

## Source and compatibility

Only original **sound** assets were available from the APK, not reusable house-animation sprites or event asset bundles. The browser smoke and lights are **new browser effects emulating animation types**, not extracted from the native game engine.

This file has not been installed into the user's Homer APK; native effect IDs, registration and object animation metadata are unavailable from the supplied APK / `assets.zip`. Do not represent it as a playable game update. No original building or save file was changed.

## Testing

Chromium browser test via Playwright set_content passed:
- Original haunted house PNG decoded at 1254x1254
- Added in town placement slot
- Tapped: 20 candy and one clue
- Night and smoke toggles
- Pause and resume
- Moved haunted house to another empty town plot
- Mobile viewport (390px) has no horizontal overflow
- No page-level JavaScript errors

Local file URL navigation and persistence across page reload could not be validated in the browser test sandbox. Test real macOS Safari separately.

## Next native step

Inspect an actual compatible, game-native building effect definition and sprite atlas from the installed cache. Map smoke anchor points, light layers, animation states and placement rewards to a new event building ID, without overwriting the original house.
