# TPA3122D2 Class D Amplifier

A stereo 15W + 15W, all through-hole Class D amplifier board built around the Texas Instruments [TPA3122D2](https://www.ti.com/lit/ds/symlink/tpa3122d2.pdf), designed in KiCad. The board is also compatible with the pin-compatible [TPA3125D2](https://www.ti.com/lit/ds/symlink/tpa3125d2.pdf) (10W stereo).

<img src="https://github.com/halherta/TPA3122D2_Amplifier/blob/main/images/TPA3122D2_AmplifierPhoto.jpg" Alt="Board Photo" width="500" />

## Overview

The TPA3122D2 is, to the author's knowledge, the only through-hole Class D amplifier IC. It comes in a 20-pin DIP package and needs only a relatively simple LC filter on its output. That makes this board a good fit for:

- A beginner-friendly soldering kit
- Learning PCB layout in KiCad (start from the provided schematic and draw your own layout)
- A compact, efficient stereo amplifier for passive speakers

**A note on part availability:** the TPA3122D2 is listed as *Active* on the TI site, but there are reports that it will move to *Not Recommended for New Designs*. The TPA3125D2 is a pin-compatible through-hole drop-in that is expected to stay active longer. It is nearly identical, except its output is rated for 10W (stereo) instead of 15W. This board can be used with either IC.

## Features

- Stereo output: 15W + 15W (TPA3122D2) or 10W + 10W (TPA3125D2)
- Supply voltage: 10 to 30 V
- Power input through a screw terminal block or a DC barrel jack
- Reverse-polarity protection on the power rails
- 3.5 mm audio jack input
- Dual-gang potentiometer for volume control of both channels
- Output LC filter as recommended in the datasheet
- 4-pin terminal block for left and right passive speakers
- Generous bypass capacitors on the supply rails and outputs
- Two SPST switches for **shutdown** and **mute** using the IC's control pins
- All through-hole parts
- 2-layer PCB, 80 mm x 80 mm

## Schematic and Layout

The schematic closely follows the recommended application circuit in the TPA3122D2 datasheet.

| Schematic | Layout | 3D View |
|---|---|---|
| [Schematic](https://github.com/halherta/TPA3122D2_Amplifier/blob/main/images/TPA3122D2_AmplifierSchematic.png) | ![Layout](https://github.com/halherta/TPA3122D2_Amplifier/blob/main/images/TPA3122D2_AmplifierLayout.png) | ![3D view](https://github.com/halherta/TPA3122D2_Amplifier/blob/main/images/TPA3122D2_Amplifier3D.png) |

## Repository Contents

| Path | Description |
|---|---|
| `TPA3122D2_Amplifier.kicad_pro` | KiCad project file |
| `TPA3122D2_Amplifier.kicad_sch` | Schematic |
| `TPA3122D2_Amplifier.kicad_pcb` | PCB layout |
| `TPA3122D2_Amplifier.kicad_prl` | KiCad local project settings |
| `Gerbers/` | Gerber and drill files for fabrication |
| `TPA3122D2LatestGerbers.zip` | Zipped Gerbers, ready to upload to a PCB fab |
| `DigikeyBom/` | Bill of materials for ordering from Digi-Key |
| `fp-info-cache` | KiCad footprint library cache |

## Getting Started

### Requirements

- [KiCad](https://www.kicad.org/) to open and edit the design

### Opening the design

1. Clone the repository:
   ```bash
   git clone https://github.com/halherta/TPA3122D2_Amplifier.git
   ```
2. Open `TPA3122D2_Amplifier.kicad_pro` in KiCad.
3. Open the schematic or PCB editor from the project window.

### Ordering the board

1. Upload `TPA3122D2LatestGerbers.zip` to your PCB manufacturer of choice (2-layer, 80 mm x 80 mm).
2. Use the files in `DigikeyBom/` to order components.

### Assembly and use

1. Solder the components, starting with the lowest-profile parts. The IC can be placed in a DIP socket.
2. Connect two passive speakers to the 4-pin output terminal block, observing left/right channel markings on the board.
3. Connect an audio source to the 3.5 mm input jack.
4. Apply a DC supply of 10 to 30 V through the terminal block or barrel jack. An old 19.5 V laptop charger works well.
5. Use the potentiometer to set the volume, and the SPST switches for shutdown and mute.

> **Tip:** Check the TPA3122D2 datasheet for supply voltage versus speaker impedance and output power limits before choosing a power supply and speakers.

## Status

The board has been fabricated, populated, and tested successfully. It amplifies audio well and gives decent sound quality and volume with a good pair of passive speakers.

## Further Reading

- [Design write-up on Hussam Talks Tech](https://hussamtalkstech.com/thruhole_classd_amp_board/)
- [TPA3122D2 datasheet (TI)](https://www.ti.com/lit/ds/symlink/tpa3122d2.pdf)
- [TPA3125D2 datasheet (TI)](https://www.ti.com/lit/ds/symlink/tpa3125d2.pdf)

## Author

[halherta](https://github.com/halherta)
