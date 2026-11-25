## 1.4.89

- Brightness and Time Travel use the same Home-wide step size across Zones. If saved Zone counts disagree and the Home has no saved count, the ruler uses 10 steps. Your saved Zone counts stay in place.
- Time Travel finds the next visible change faster when several Rooms are already at full brightness.
- Your existing Hue dimmer button mappings stay in place when you update.
- Emergency ends when you release the last Room still held in Emergency.

### Highlights

- [small] Fixes lights that could stay stuck after a late On or a scene change.
- [small] Time Travel responds faster in large homes.
- [small] Brightness steps feel the same in every Zone, even ones with a narrow range (after an App update).
- [small] Emergency mode ends by itself once every Room is back to normal (after an App update).
- [small] New homes get a simpler Hue dimmer button layout.
- [small] The App tells you when a Brain update is ready (after an App update).

## 1.4.88

- Emergency now covers the whole home: one hold turns every Room on full bright, and End returns each Room to what it was doing.
- Switch presses no longer wait behind background saves.
- Presses right after a restart work sooner; until Home Assistant confirms a light group, lights are sent one by one.
- Time Travel and brightness taps move to the next change you can see. Time Travel keeps working in a pinned Room that is off or has only on/off lights.
- Set how clear or cloudy the sky is from the App, for 1, 2 or 4 hours or until tomorrow.
- The sun's full-strength level is now 40% for everyone.
- The App shows which Rooms and controls still need setting up, and why a sensor can't act.
- Installs check that Rooms, Zones, schedules, Moments and controls come through an update unchanged.

### Highlights

- [small] Every Time Travel and Brightness tap now makes a change you can see.
- [headline] Set how clear or cloudy the sky is from the App.
- [small] See which Rooms and controls still need setup, and why.
- [small] Updates keep your Rooms, Zones, schedules, Moments and switches.

## 1.4.86

- Keep Brain data in the add-on's own configuration directory, with verified migration from the previous location and clearer recovery warnings.
- Show supported power-recovery settings and recent Zigbee signal facts in device details. Place a No-Room light into a Room, or Identify it independently.
- Lights with no usable name show a tidy name built from their id.
- Re-check a Zigbee bulb's power-on setting when it comes back.
- Preserve an accepted Contact-close Off through a registry gap, while respecting reopened doors and current Room membership.
- Let periodic group updates serve healthy lights while a busy bulb keeps its own recovery work.
- Follow Home Assistant registry changes automatically when Room light membership changes, preserving Section and Layer settings.
- Expose the Room switch Off-after setting, show ordered Control setup reasons, and use five seconds as the default teaching-note window.
- Let negative Balance reduce brightness below the curve minimum, including NiteLite and Pins, while preserving hard light limits.
- Record Activity through a background store and keep related Home, Room, Section and Control views consistent.
- Change the Return pace without jumping the current adjustment. Reset ignores tiny residual adjustments and preserves active Pins.

## 1.4.85

- Keep ordered Manage lights edits atomic and check every operation against a pending Room move.
- Keep admitted Contact-close Off actions through intervening actions, while respecting other open doors and the current Reach.
- Seed Inside and Outside on fresh Homes, report Rooms that have not started, and support switch-level Also off plus bulk Control duty changes.
- Follow current Control names and return the saved Controls basis with Undo replies.
- Report coherent Room, Section and Main fade brightness samples and landing targets.
- Offer Room Glo up only when that Room has its own adjustment or Pin.
- Supply the Home's upcoming and recent timezone offset changes and save the Sun-exposure journey flag independently of the Balance journey flag.
- Retain the accepted startup logging and architecture recipe improvements. Image and target qualification remain separate release gates.

## 1.4.84

- Restored the 1.4.83 image recipe. Home Assistant's standard multi-architecture YAML recipe and local amd64 builds are deferred to Brain185, using Supervisor-compatible tag pins and a post-build base-digest check.
- Lights returning after a power cut receive their current intended settings. Returning lights in the same Room share the recovery calculation.
- Brightness calculations keep their precision until the final whole-percent light level. Room Full follows the Room's Standard lights while preserving separate Section adjustments.
- Time Travel preserves stamped Room and Zone Color adjustments, including long Pins that cross a restart boundary.
- Section NiteLite and BriteLite use the Room preset when the rest of that Room is off, leaving only the selected Sections on.
- Hue Hub switches follow the revised tap and burst rules, with repeated brightness and Color steps and bounded recovery for an unmatched release. Eligible Zigbee single actions can run without waiting for their trailing summary.
- Pin previews and feedback choose eligible lit lights in the first lit Room in the Reach.
- The App can show when a whole-Room fade is due to finish. This reports the Room's fade clock.
- Settings reads yield between bounded pieces of work. A frozen Brain event loop can exit for an in-place service restart, with a repeated-exit guard.

## 1.4.83

- Fixed missed presses and false double presses from switches paired through a Hue Hub.
- Hue Hub lights that miss an Off are now corrected within a few seconds, not about 20.
- Changing a Room or Section ends that Room's fade, whether it is fading on or off. Zone changes and Quick Wake or Bedtime let Room fades continue. A press that changes nothing never ends a fade.
- Fixed Time Travel reporting "No change" too soon during a fade.
- Dimmer can go down to 1%, even when the Zone's curve minimum is higher. Time Travel and NiteLite still follow the curve.
- Quick Wake and Quick Bedtime now Pin the Zone until Wake or Bedtime, instead of Pinning each Room.
- Time Travel on a Section switch now moves the whole Room when the rest of that Room is off. Otherwise the switch shows "can't do that".
- Switch cues: the Reach-number blink and "can't do that" use the switch's cue light (Automatic picks from its first Reach). Pin and hold cues blink inside the current Reach. Rooms no longer have their own cue light setting.
- Identify flashes the chosen light strongly for about five seconds. Tap again to stop, or choose another light.
- Off-duty switches and sensors still show when they were last used, without changing any lights.
- Motion and contact Reaches that were switched off or set to "Do nothing" are removed. A sensor left with none goes off duty.
- Changes to the Home Assistant add-on options now take effect on restart.
- Older Reaches can be opened and edited on the same Reach page.
- The Controls list loads faster.
- Adding a new or found Room to a Zone leaves it off duty until you turn it on duty.
