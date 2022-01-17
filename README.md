# MacGuevar PS3 Fighting Board

Fork of [bootsector's PS3PadMicro](https://github.com/bootsector/PS3PadMicro).

A few mods and quality of life features that have been implemented on top of the original code;

- 1 ms polling;
- SOCD cleaner for use with hitboxes / mixboxes;
- Pinout compatible with [DaemonBite's Arcade Encoder](https://github.com/MickGyver/DaemonBite-Arcade-Encoder);
- Home button gets its own pin;
- *Switch0* to choose between Left Stick and Digital Pad;

Still to do;

- Autofire / Turbo with LED indicator;
- *Switch1* switch to choose between *Normal* and *Tournament* mode (Start, Select, and Home disabled in Tournament mode);
- PCB for easy connection in actual fightsticks;
- Measure input lag.

### Pinout / Wiring
![MacGuevar PS3 Fighting Board](/docs/pro_micro_pinout.jpg)

All easily accesible pins are currently in use, 2 more are available if the bottom resistors next to the crystal are removed.

A possible way forward would be setting up Switch1 where Switch0 currently is to toggle Tournament mode. Then implementing some button combinations to choose between Left stick, D-pad, and Right stick. This would maximize functionality and avoid unintentional changes while playing.

Autofire and its LED would need access to the 2 extra pins.

### Why did I bother with this fork?
I was using DaemonBite's Arcade Encoder (DBAE) quite happily, but after getting my hands on a *Brook Wingman SD* adapter for Dreamcast / Saturn and realizing they didn't work together I was bummed.

bootsector's PS3PadMicro did work with the adapter, so I decided to modify it to fit my "needs".
