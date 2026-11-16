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
