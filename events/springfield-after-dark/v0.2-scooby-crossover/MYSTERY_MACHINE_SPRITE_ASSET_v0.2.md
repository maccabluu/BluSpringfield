# Mystery Machine replacement art asset v0.2

## What changed

The previous browser preview used a simplistic box-like van, which the user rejected. It has been replaced with a three-quarter **isometric** vector sprite better aligned to the approved Haunted Cottage perspective. The exterior includes a shaded turquoise roof, green body, outlined side/front glazing, orange flower graphics, side logo, rotating wheel details and an operable side door.

## Delivered in conversation

- `BluSpringfield_Scooby_Act1_Mystery_Machine_Art_v0.2/Mystery_Machine_Act1_Test_v0.2.html` for interactive arrival, placement, door, headlights and quests.
- `BluSpringfield_Scooby_Mystery_Machine_Isometric_v0.2.zip` including original SVG source, 1520×920 transparent PNG, eight driving animation frames, four door animation frames, transparent sprite atlases and JSON animation metadata.
- The approved Haunted Cottage stays embedded unchanged in the test.

The source assets are in the attached ZIP, **not copied as binary files into GitHub**. This document records the output and integration status, not a fully merged game asset.

## Validation

- Chromium browser checks: arrival, door opening, parking, candy collection and no uncaught JavaScript errors.
- Desktop and 390px mobile layout checks: no horizontal overflow.
- SVG XML validates, transparent PNG exported, 8 drive frames and 4 door frames with spritesheet metadata.

## Using animation from the original Homer game

The existing user-uploaded **APK and assets.zip** include general core interface graphics and sounds but **do not contain the downloaded character animation atlas/state data**. This is a confirmed file inventory limit, not a promise to extract inaccessible files. None of the van/character visual animation frames in the browser preview are copied from the game's native resources.

The preview uses original Homer audio for placement and rewards. Vehicle movement, door and wheel loop are newly authored browser effects and exported sprite frames. Scooby and Shaggy still require separate character sprite artwork and compatible animation state definitions, which are not present in the files supplied.

## Native integration blockers

1. Need actual downloaded game resources for character idle/walk/run animations and atlas format.
2. Identify resource registration and footprint schema for `cross_mystery_machine`.
3. Connect vehicle sprite atlases to native animation engine.
4. Create Scooby/Shaggy character sprite atlases with walk/idle/scared/eat states, using verified game-native animation controller timings once available.
5. Test Android game loading, original town preservation, save migration and signing. No working Homer APK has been built or installed yet.

Status: **Improved browser asset and sprite pack. Character native animation integration is blocked.**
