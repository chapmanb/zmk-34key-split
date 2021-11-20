## Build and configuration for small 34 key split wireless keyboards

To treat wrist and elbow RSI issues caused by too much time programming, I
ended up using ergonomic mechanical keyboards with the following properties:

- Split: two halves, allowing shoulder width spacing to prevent hunching
- Low profile: lower keys and base, encouraging hand hovering to prevent wrist
  bending that occurs with higher keyboards.
- Thumb cluster: transfer pressing of common keys to your stronger thumbs
- Small: less keys avoid reaching, especially with your weaker pinky fingers.
  See this detailed description of the [Absolem](https://zealot.hu/absolem/)
  keyboard for a nice description of the benefits of avoiding excessive finger
  travel.
- Ortholinear and staggered: fits better with natural curve of your hand.
  Stagger helps spread out your hand, giving many of the benefits of tenting
  your keyboard in a simpler setup.
- Programmable: place keys in layers and locations based on usage, avoiding
  scrunching and uncomfortable positions for common actions.

Practically, there are many different keyboard choices you can assemble
with these and overlapping properties thanks to the great open communities like
[ErgoMechKeyboards reddit](https://www.reddit.com/r/ErgoMechKeyboards/) and
[Low Profile Keyboards discord](https://discord.gg/W5qnkqbteT). I started off
with a commercially available [ErgoDox EZ](https://ergodox-ez.com/), which is a
great board for learning to use thumb clusters, remapping your key layouts and
getting comfortable with ortholinear keys. As I began to head back to the
office, I wanted to get comfortable with a more portable keyboard.

I settled on 34 key boards with 5 columns of 3 keys each and 2 thumb keys on
either side. These meet the above criteria and are also easier to assemble since
commonly available microcontrollers can map directly to each key without needing
harder to assemble diodes or secondary chips. Using wireless microcontrollers,
they are small and easy to carry between multiple work offices and home. The
details below helped me build 3 different related boards with unique tweaks:

- [Sweep](https://github.com/tapioki/cephalopoda/tree/main/Architeuthis%20dux)
  -- 34 keys using principles from the
  [Ferris](https://github.com/pierrechevalier83/ferris) but using a single
  controller and no diodes: low profile, with lower pinkies; has power and reset switches
- [Hypergolic](https://github.com/davidphilipbarr/hypergolic) -- 34 keys with
  aggressive stagger and lower pinkies, but without wider thumbs; has power and
  reset switches
- [A dux](https://github.com/tapioki/cephalopoda/tree/main/Architeuthis%20dux)
  -- 34 keys with aggressive stagger, even lower pinky keys and wider thumbs; no
  power or reset switches

## Building

The unique aspect of all these boards is that they require fewer parts, making
them a nice entry point for a non-electronics skilled person like myself. This
section has links to resources that were useful for me: US based and unskilled
in keyboard building.

For the keyboard you need to obtain:

- PCBs
- Controllers
- Controller sockets and batteries
- Switches
- Keycaps
- Reset and on/off switches
- Bumpers -- I used [small rubber stick on bumpers](https://www.adafruit.com/product/550) 
  on the bottom of the PCB for
  protection and to keep from sliding around. Another nice looking inexpensive
  bottom protection choice is using a
  [mousepad for a base](https://www.reddit.com/r/ErgoMechKeyboards/comments/mpp2g9/wireless_ferris_sweep_compact/).

For soldering gear, [Adafruit has some great
recommendations](https://www.adafruit.com/product/136). The tools I found
indispensable were the soldering iron, solder sucker, diaganol cutters and wire strippers.

## Software
