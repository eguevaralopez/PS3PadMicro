# MacGuevar PS3 Fighting Board

Fork of [bootsector's PS3PadMicro](https://github.com/bootsector/PS3PadMicro).

A few mods and quality of life features that have been implemented on top of the original code;

- 1 ms polling;
- SOCD cleaner for use with hitboxes / mixboxes;
- Pinout compatible with [DaemonBite's Arcade Encoder](https://github.com/MickGyver/DaemonBite-Arcade-Encoder);
- Home button gets its own pin;
- *Switch0* to choose between *Normal* and *Tournament* mode (Start, Select, and Home disabled in Tournament mode);
- Button combinations to choose between Left Stick and Digital Pad;

### Wiring and usage
![MacGuevar PS3 Fighting Board](/docs/pro_micro_pinout.jpg)
- Switch0 toggles Tournament mode
- Home + Select = Left Stick
- Home + Start = D-Pad

### Why did I bother with this fork?
I was using DaemonBite's Arcade Encoder quite happily, but after getting my hands on a *Brook Wingman SD* adapter for Dreamcast / Saturn and realizing they didn't work together I was bummed.

bootsector's PS3PadMicro did work with the adapter, so I decided to modify it to fit my "needs".

### To-do

- Add a dedicated *Mode* button to activate different settings:
  - Mode + Select = Left Stick
  - Mode + Start = Right Stick
  - Mode + Home = D-pad
- Autofire code with LED indicator;
  - Mode + [button] = autofire [button]
  - LED solid when autofire is active on some button, flashes when button w/ autofire is pressed, off when no autofire is in place.
- PCB for easy connection in actual fightsticks;
- Measure input lag.

All easily accesible pins are currently in use, 2 more are available if the bottom resistors next to the crystal are removed. Moving Switch0 to one of these "extra" pins allows the use of *D5* for the Mode button. This makes it possible to have most intended functionality without modifying the Arduino, leaving Tournament Mode and the Turbo LED as optional features that require board modification.
