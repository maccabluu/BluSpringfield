# Springfield After Dark: Mystery Inc. Files

## Big update proposal (v0.2)

A **28-day, four-act Scooby-Doo crossover** designed for the user's existing **Homer** / BluSpringfield app. **Design only**, not a working APK. Keep the v0.1 pumpkin event and six existing story quests as optional prologue content. The main crossover has **20 new quests**, five unlockable Mystery Inc. characters, three character costumes, ten outdoor building concepts and 26 decorations.

### The story

The Halloween pumpkins begin flickering, ghosts haunt Evergreen Terrace, and the Mystery Machine parks outside Homer’s house. Fred thinks the haunting is staged. Velma and Lisa examine strange mechanical marks. Bart sees a chance to prank Springfield, while Homer only wants the candy back. An early ghost is exposed as Milhouse, but the actual Phantom is still at large. The gang traces remote-controlled ghost drones to the power plant and a film backlot. The final unmasking reveals Mr. Burns, who tried to scare residents away from property he wanted to redevelop. The ending leaves one genuinely unexplained donut-shaped apparition.

### Four acts

#### Act 1. The Mystery Machine Arrives (Days 1–7)
A mysterious green van rolls into Springfield while flickering pumpkins and runaway ghosts frighten Homer. The gang sets up a temporary investigation base.

1. **Strangers on Evergreen Terrace**. Cast: Homer. Tasks: Inspect Halloween decorations; place one glowing pumpkin. Unlock: Mystery Machine, placeable vehicle.
2. **Like, Zoinks!**. Cast: Shaggy and Scooby. Tasks: Collect 5 wandering ghosts; send Homer on a 1-hour candy search. Unlock: Playable Shaggy and Scooby.
3. **Jinkies at Midnight**. Cast: Lisa and Velma (visiting NPC). Tasks: Collect 3 clue drops; have Lisa research footprints. Unlock: Mystery Clue Board decoration.
4. **A Trap That Almost Works**. Cast: Bart, Shaggy and Scooby. Tasks: Complete Bart's prank job; place 3 cobweb fences. Unlock: Spooky Streetlamp decoration.
5. **The House With Glowing Windows**. Cast: Homer, Shaggy and Scooby. Tasks: Investigate two nearby houses; earn 250 total candy. Unlock: Haunted Simpsons House exterior variant.

#### Act 2. The Schoolhouse Ghoul (Days 8–14)
A bell rings from the empty school and a masked ghoul appears. A smaller prank is exposed, but the real Phantom slips away.

1. **The Bell That Rings Alone**. Cast: Lisa and Bart. Tasks: Examine the school bell; collect 4 clue drops. Unlock: Broken Bell decoration.
2. **Footprints in the Playground**. Cast: Shaggy and Scooby. Tasks: Follow glowing footprints; catch 6 ghosts. Unlock: Glowing Paw Prints decoration.
3. **Fred's Excellent Trap**. Cast: Fred and Daphne (visiting NPCs). Tasks: Place a trap net; complete a trap-preparation job. Unlock: Playable Fred and Daphne.
4. **School's Out, Ghosts In**. Cast: Lisa, Fred and Daphne. Tasks: Complete two school investigations; place a fog machine. Unlock: Haunted Springfield Elementary exterior variant.
5. **The First Unmasking**. Cast: Bart and Mystery Inc.. Tasks: Complete the playground chase; find 5 clue drops. Unlock: Spectral Milhouse costume and 150 candy.

#### Act 3. The Reactor Riddle (Days 15–21)
The gang traces strange footprints, glowing slime and mechanical noises to the Power Plant. Lisa finds evidence of remote-controlled ghosts.

1. **Nuclear Nightmares**. Cast: Homer and Lisa. Tasks: Investigate the Power Plant exterior; find 4 clues. Unlock: Reactor Warning Sign decoration.
2. **The Velma Equation**. Cast: Velma and Lisa. Tasks: Complete Lisa's research job; inspect 2 slime puddles. Unlock: Playable Velma.
3. **Scooby-Doo, Where'd You Go?**. Cast: Scooby and Shaggy. Tasks: Catch 10 roaming ghosts; finish a Scooby chase job. Unlock: Scooby Snack Cart building.
4. **Trouble in the Cooling Towers**. Cast: Daphne and Fred. Tasks: Place 2 glowing barrels; set 2 outdoor traps. Unlock: Haunted Reactor exterior variant.
5. **The Phantom's Signal**. Cast: Velma and Lisa. Tasks: Collect 8 clues; investigate a ghost drone. Unlock: Phantom Signal Antenna decoration and 200 candy.

#### Act 4. The Phantom of Springfield (Days 22–28)
The gang traps a masked figure after tracing the mechanical ghosts to a deserted film set. Mr. Burns is exposed as the mastermind of a scare scheme.

1. **The Old Backlot**. Cast: Fred and Daphne. Tasks: Build the outdoor Phantom Backlot; inspect 3 props. Unlock: Phantom Backlot building.
2. **Five Scooby Snacks and a Plan**. Cast: Shaggy and Scooby. Tasks: Collect 5 snack drops; craft 3 trap parts. Unlock: Mystery Inc. Trap Workshop building.
3. **Operation Unmask**. Cast: Fred, Daphne, Velma and Lisa. Tasks: Place 3 traps; complete a 4-hour decoy job. Unlock: Unmasking Stage decoration.
4. **The Phantom Chase**. Cast: Homer, Bart, Scooby and Shaggy. Tasks: Win three non-combat ghost-trap phases. Unlock: Phantom Costume for Mr. Burns.
5. **And I Would Have Gotten Away With It...**. Cast: Whole cast. Tasks: Read final unmask dialogue; place the commemorative Mystery Plaque. Unlock: Mystery Inc. Detective Office and event completion.

### Character unlocks

- **Scooby-Doo**: cross_02. stand, walk four directions, sniff, run scared, eat snack, tail wag, tap reaction. Animation plan: new animal sprites mandatory; possible reuse of timing/state framework only.
- **Shaggy Rogers**: cross_02. idle, walk, run, eat, scared, trap distraction. Animation plan: adapt humanoid movement timing, redraw frames.
- **Fred Jones**: cross_08. idle, walk, inspect, set trap, run. Animation plan: adapt humanoid timing and generic trap/interaction effects.
- **Daphne Blake**: cross_08. idle, walk, investigate, decoy, run. Animation plan: adapt humanoid timing, redraw frames.
- **Velma Dinkley**: cross_12. idle, walk, inspect clue, find glasses, run. Animation plan: adapt humanoid timing, redraw frames.
- **Spectral Milhouse**: cross_10. idle, walk, nervous gesture. Animation plan: possible Milhouse base sprite state set if a compatible authorised reference exists.
- **The Phantom (Mr. Burns)**: cross_19. hover illusion, idle, walk, unmask. Animation plan: possible existing Burns sprite states plus overlaid costume, engine support unverified.
- **Ghost Hunter Homer**: optional side-task. idle, walk, inspect, eat candy. Animation plan: possible Homer base sprite states with new props.

### Buildings (all outdoor)

- **The Mystery Machine**: existing vehicle base to inspect (geometry may not suit the van). New item ID `cross_mystery_machine`. Animation: headlight flash and door open.
- **Haunted Simpsons House**: Simpsons House geometry as a separate variant. New item ID `cross_haunted_simpsons_house`. Animation: flickering windows and chimney smoke anchored to chimney.
- **Haunted Springfield Elementary**: Springfield Elementary geometry as a separate variant. New item ID `cross_haunted_school`. Animation: flickering bell/window light.
- **Haunted Reactor**: Nuclear Power Plant silhouette/roofline as a separate variant. New item ID `cross_haunted_reactor`. Animation: reactor window pulse and low smoke.
- **Phantom Backlot**: Krustylu Studio geometry as a separate variant. New item ID `cross_phantom_backlot`. Animation: stage lamps and fog.
- **Scooby Snack Cart**: an existing exterior stall as a base. New item ID `cross_scooby_cart`. Animation: steam and serving hatch.
- **Mystery Inc. Trap Workshop**: an existing small shed/workshop as a base. New item ID `cross_trap_workshop`. Animation: subtle light/prop loop.
- **Mystery Inc. Detective Office**: an existing storefront as a base. New item ID `cross_detective_office`. Animation: subtle light/prop loop.
- **Haunted Snack Shack**: existing v0.1 concept; look for compatible food kiosk. New item ID `sad_haunted_snack_shack`. Animation: subtle light/prop loop.
- **Abandoned Costume Shop**: an existing shopfront or boarded-up store. New item ID `cross_costume_shop`. Animation: subtle light/prop loop.

### Decorations

Glowing Pumpkin, Cobweb Fence, Ghost Tree, Mystery Plaque, Candy Cauldron, Spooky Streetlamp, Fog Machine, Mystery Inc. Sign, Crime Scene Tape, Mystery Clue Board, Evidence Marker, Dropped Scooby Snacks, Glowing Paw Prints, Coffin Prop, Slime Puddle, Haunted Tombstone, Monster Footprints, Broken School Bell, Haunted School Banner, Flickering Porch Lamp, Mechanical Ghost Drone, Reactor Warning Barrel, Reactor Warning Sign, Trap Net, Unmasking Stage, Phantom Signal Antenna.

### Core loop

Collect Halloween Candy from quests, tappable roaming ghosts and daily jobs. Clue drops feed each mystery's progress tracker. A **non-combat three-phase ghost trap sequence** forms the Act 4 finale. All earned rewards are permanent. Candy milestones at 50, 150, 300, 600 and 900 retain the existing v0.1 prizes. New milestones: 1200, 1600, 2200, 3000 and 4000 candy. Some buildings and characters also unlock from quests directly. Use new inventory IDs to avoid duplicate-award bugs.

### Reusing the Homer app's existing buildings and animations

1. Inspect an original building sprite, animation metadata, pivot, tile footprint, object ID, render layers and frame timings.
2. **Duplicate its permitted art and metadata into new event-specific IDs.** Leave the original building and its permanent placement untouched.
3. Rework its roof, signage, lighting and props into a haunting variant; check proportions in the actual town camera.
4. Where possible, reuse **effect logic and timing** for smoke, light flickers, tap feedback, walking and construction. Verify the engine supports the target before copying. Re-anchor smoke to the actual chimney.
5. Do **not** assume a human character animation can directly power Scooby; he needs bespoke quadrupedal sprite frames even if the engine's animation controller is reused.
6. The Mystery Machine requires new exterior sprite artwork even when a generic in-game van supplies scale and shadow references.
7. New costumes may share compatible state machines with existing Homer, Bart, Burns or Milhouse characters, but every state requires verified atlas or skeleton compatibility.
8. Missing game cache/content definitions prevent reliable native integration today. The existing APK and user-supplied `assets.zip` did **not** contain the required `SpecialEventList.xml`, master lists and compatible character/building object data. No existing asset was successfully cloned into the app yet.

### Recommended implementation order

1. Finish and verify **one pumpkin as a native placeable decoration** (sprite atlas, footprint, save/load, tapping and motion).
2. Clone an **existing small outdoor building** into a new unique event item and prove both original and new building coexist.
3. Establish an effect/animation compatibility table using the real cached asset definitions.
4. Convert the Mystery Machine and haunted house designs into proper sprite/atlas files.
5. Implement the event menu and a minimal two-quest vertical slice with Homer and one Mystery Inc. character.
6. Expand to all 20 quests, prizes, five characters, buildings and final trap sequence.
7. Run regression checks for app restarts, old town saves, calendar handling, quest counters and update signing.

### Status

`prototype-not-integrated`. These are design specifications only. No actual Homer APK or saved Springfield was modified. Copyright and other release rights for both franchises need verifying before distributing the crossover publicly.
