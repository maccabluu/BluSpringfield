# Act 1: Mystery Machine Arrival Test v0.1

## Deliverable

A complete offline HTML browser test and a ZIP with source media were generated in the conversation:
- `BluSpringfield_Scooby_Act1_Mystery_Machine_v0.1/Mystery_Machine_Act1_Test.html`
- `BluSpringfield_Scooby_Mystery_Machine_Act1_Test_v0.1.zip`

The ZIP includes the previously approved Haunted Cottage illustration, hand-authored SVG Mystery Machine van, original game WAV files for interaction sounds, 3 interactive quests and `manifest.json`.

## Original Homer APK resources actually reused

Source: the user-supplied `BluSpringfield-Offline-Test-unsigned(1).apk`, nested archive `assets/audio/res-audio/1`.

Five audio files were extracted and verified byte-for-byte:
- `103_drop_building.wav`, building placement
- `05_reward_collect.wav`, collection
- `16_quest_complete.wav`, quest completion
- `01_general_button.wav`, general action
- `08_confirm_bldng.wav`, confirmation

**Game-native vehicle/building animation frames reused: none.** The available APK and matching `assets.zip` have no downloaded vehicle, building, event or character animation bundles necessary to implement native animations. The browser tester's van arrival, light flash, door opening, exhaust, wheel spin and house smoke/flicker were created in SVG/CSS. Never represent those visuals as extracted animations from Homer.

## Browser test behaviour

- Mystery Machine drives into the scene; its door opens and closes
- Three parking locations; the approved haunted cottage remains in place
- Investigating the house awards 20 candy and a clue
- First three quests of the Scooby-Doo crossover with dialogue and candy rewards
- A timed Shaggy investigation task
- Night/smoke/lights toggles, animation pause, local-only test reset
- Isolated localStorage key used for preview progress

## Verified test results

- JavaScript syntax validated with Node
- Chromium browser tests at desktop (1365 px) and phone (390 px) passed: arrival, parking, door, investigations, completing first two quests, night mode, no horizontal overflow, no uncaught JavaScript errors
- Separate complete-flow browser test passed all 3 quests and their rewards, no uncaught JavaScript errors
- Both screenshot renderers displayed the actual approved haunted house and coded Mystery Machine
- File-URL navigation and persistence across reloaded local files were blocked by the test environment and therefore are not claimed verified
- No APK modification or BlueStacks installation performed

## Native integration outstanding

1. Obtain existing downloadable game content or a working editable native resource/animation bundle, including vehicle and building atlas formats and action timelines.
2. Convert the approved art into the real native asset format with consistent pivots, collision and sprite transparency.
3. Register unique event vehicle/building IDs, with the original house/building unchanged.
4. Map game-native animation controllers to available effects. Do not invent or mislabel asset reuse.
5. Hook actual native quests, inventory and saved progress, then test in BlueStacks using the original signing key.
6. Confirm rights for public distribution of both franchise assets and audio before any public release.

Status: **Working browser prototype only. Not integrated with the installed Homer game.**
