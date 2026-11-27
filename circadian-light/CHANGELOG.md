## 1.4.91

- Hue lights can turn on without waiting for the Zigbee fade in a mixed Room.
- Emergency Start uses confirmed light groups. Follow-up checks reach lights that missed the first pass or came back online during Emergency.
- Eligible motion, switch and App commands can retry when the light map changes before a send.
- Switch holds keep working through light-map updates when the Room still contains the same lights.
- Recover missing Room and Zone memory from a saved copy and show a notice in the App.
- Moment usage shows the switch button that runs the Moment.

## 1.4.90

- Emergency End fades lights back over ten seconds. Emergency Start uses the normal turn-on fade, capped at one second.
- Open the HomeGlo panel inside Home Assistant to manage Zone order and edit Layers.
- Use the compiled Brain on 64-bit ARM and x86 add-on images.
