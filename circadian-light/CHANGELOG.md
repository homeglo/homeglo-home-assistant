## 1.4.90

- Emergency End fades lights back over ten seconds. Emergency Start uses the normal turn-on fade, capped at one second.
- Open the HomeGlo panel inside Home Assistant to manage Zone order and edit Layers.
- Use the compiled Brain on 64-bit ARM and x86 add-on images.

## 1.4.89

- Brightness and Time Travel use the same Home-wide step size across Zones. If saved Zone counts disagree and the Home has no saved count, the ruler uses 10 steps. Your saved Zone counts stay in place.
- Time Travel finds the next visible change faster when several Rooms are already at full brightness.
- Your existing Hue dimmer button mappings stay in place when you update.
- Emergency ends when you release the last Room still held in Emergency.
