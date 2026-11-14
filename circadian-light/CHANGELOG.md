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
