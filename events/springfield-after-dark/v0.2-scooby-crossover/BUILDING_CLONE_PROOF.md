# Building clone proof: Haunted Cozy Cottage

Status: **browser prototype tested; not integrated into Homer APK**.

## What was built

- The base design is the **Cozy Cottage** in `dlc/living-springfield/v0.1`, referenced without changing the original.
- A separate Halloween object ID: `cross_haunted_cozy_cottage`.
- New browser vector concept using the same house geometry, with boards, cobwebs, purple walls, glowing windows, chimney smoke and ghost-orb details.
- Offline interactive proof: Add Haunted Cottage, choose one of two empty town slots, move only the haunted copy, tap it for a clue and 20 Halloween Candy, use night mode or disable animated effects. The base cottage stays fixed.
- Client-side test stores placement, currency, clues and night preference in localStorage when allowed by the browser.

## Verification

A Chromium browser smoke test using in-memory page content **passed** these interactions: normal cottage retained, haunted cottage placed, first clue tap pays 20 candy, night mode enabled, new copy moved, and mobile screen has no horizontal overflow. JavaScript produced no uncaught errors in that test.

Browser file navigation and HTTP URL loading were blocked by the testing environment, so persistence across a real URL reload and macOS Safari behaviour are **not claimed tested**. The generated test HTML and ZIP were delivered as sandbox attachments in the conversation, not committed into the game runtime.

## Asset/animation caveats

- These are drawn browser SVG illustrations, **not original game sprite atlas assets**.
- Smoke and flicker are **new CSS effects**, not reused native game animation bundles.
- The asset sheet titled `Cozy Cottage Game Asset Sheet.png` was inspected as a scale/shape reference, but the actual game-native atlas format and compatibility are unknown.
- Tile footprint `[6,5]` comes from the existing prototype manifest and is **not verified against the actual Homer app**.

## Native action list

1. Locate real downloaded building and animation definitions for the installed game; existing APK and the previously uploaded `assets.zip` lack the required master lists.
2. Identify exact object registration, atlas format, pivot, z-index, footprint and collision conventions.
3. Clone an authorised in-game building asset to `cross_haunted_cozy_cottage` while leaving the original ID intact.
4. Map the haunted sprite states and effects, align chimney smoke anchors to the roof, and test on the native renderer.
5. Hook native placement, event inventory, quest counter, offline save and reward collection.
6. Validate signing and an update on BlueStacks without deleting game progress.

No installed app or save data was changed.
