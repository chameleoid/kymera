# About the Kymera wearables

Kymera werables are designed from the ground up to be affordable assistive
technology devices with a focus on durability, upgradability, and
user-extensibility.  To this end the Kymera wearables are developed as
open-source hardware, with the idea that the source provided can be used to
build an ecosystem of extensible assistive technology wearables.

These werables use [Haptic Braille](#haptic-braille) to provide users constant
access to information without the need to view a screen.

This is the main repository for the Kymera wearables, which functions as a
starting point for newcomers and central area for issue tracking.  For source
code, or to place a pull request, please check out one of the related
repositories:

- Core library [@kymera/core][]
- Simulator app [@kymera/simulator][]

[@kymera/core]: https://gitlab.com/chameleoid/kymera/core
[@kymera/simulator]: https://gitlab.com/chameleoid/kymera/simulator


## Development Boards

Minimum Hardware Features:
- 3 haptic feedback vibrators or actuators; required for Haptic Braille
- 3 hardware buttons

Preferred Features:
- 8 haptic feedback vibrators or actuators
- 3 hardware buttons
- For TTS support, an SBC with a minimum of 256MB of RAM is recommended

Supported SBCs:
_TBD_
<!--
- OMEGA2+
- Pi Zero W
- Banana Pi BPI-M2 Zero
-->


## Haptic Braille
Haptic Braille is an inexpensive Braille character interface that utilizes a
series of haptic points to form a Braille cell.  This interface can be used to
receive textual information without needing to look at a screen or listen for
audible cues, and can be worn anywhere with sufficient nerve density.

Haptic Braille comes in three forms; [Full-Cell](#full-cell-haptic-braille),
[Split-Cell VI](#varying-intensity), and [Split-Cell VC](#varying-cadence).

### Full-Cell Haptic Braille
Full-cell Haptic Braille pulses each cell to an array of haptic feedback
vibrators or actuators.

### Split-Cell Haptic Braille
Split-cell Haptic Braille cuts each cell into two sections (left/right halves),
reducing the minimum number of vibration sources to three.  Cells are then
rendered using one of two methods: varying intensity, or varying cadence.

#### Varying Intensity
The first half of a cell uses light pulses to mark empty
dots, and regular pulses to mark filled dots.  The second half of a cell uses
regular intensity pulses to mark empty dots, and heavy pulses to mark filled
dots.

#### Varying Cadence
Like the first method, light pulses mark empty dots, and
stronger pulses mark filled dots.  The pause duration between the first and
second half of the cells are timed at 2/3 the pause duration between cells.
Ex: If the pause between cells is set to 300ms, the pause between cell halves
would then be 200ms.


## Text-to-Speech
Kymera wearables use Mimic for TTS capabilities due to its ease of use and
relatively low system requirements.  At the moment we're looking to find ways
to synchronize speech synthesis and Braille output.
