# Event 001: Springfield After Dark

A first-event prototype for **BluSpringfield**, designed as a two-week outdoor Halloween update.

## Player experience

Start from the event banner. Homer notices odd decorations, Bart chases ghosts, Flanders keeps watch, Lisa investigates, and Marge prepares a candy stall.

Earn Halloween Candy by:
- Completing timed character jobs
- Tapping wandering ghosts around the outdoor town
- Claiming a daily participation bonus
- Completing six sequential quests

Candy is tracked as **cumulative earned**, not spent. Claim permanent prizes at 50, 150, 300, 600 and 900 candy: glowing pumpkin, four cobweb fence pieces, ghost tree, haunted snack shack, and a Vampire Bart costume. The final quest also awards an event plaque.

The event runs for 14 days **from activation on the player's device**. It does not depend on an external server or fixed calendar dates. When the event ends, newly earned candy stops but rewards remain in the local save.

## Files

- `event.json`: timing, jobs, currency, unlocks, progression and local-save requirements.
- `quests.json`: six stages with dialogue, completion requirements and rewards.
- `asset-manifest.json`: sprite and animation requirements for the outdoor town.
- `preview.html`: optional browser prototype to click through the event loop. Placeholder emojis are not finished art.

## State and integration

**Status: prototype-not-integrated.** The `maccabluu/BluSpringfield` repository currently contains DLC prototypes rather than the game client/runtime. These event definitions and browser preview do not update or patch the installed Android APK.

Before release, implement native event banner, local quest counters, timed jobs, offline local saves, reward inventory, prize placement and art integration. Test restarting the game, changing date/time, cancelling a job, full inventory, repeat tapping and event expiry. Keep original installed progress intact. No home interiors.
