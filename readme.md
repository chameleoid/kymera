# Aboyt the Kymera wearables.

Kymera werables are designed from the ground up to be affordable assistive
technology devices with a focus on durability, upgradability, and
user-extensibility.  To this end the Kymera wearables are developed as
open-source hardware, with the idea that the source provided can be used to
build an ecosystem of extensible assistive technology wearables.

These werables use [Braille](#split-cell-haptic-braille) to provide users
constant access to information without the need to view a screen.


Minimum Hardware Features:

- 3 haptic feedback vibrators or actuators; required for Haptic Braille
- 3 hardware buttons
- Bluetooth
- Pi Zero W, or better



## Split-Cell Haptic Braille
Split-cell Haptic Braille cuts each cell into two sections (left/right halves),
reducing the minimum number of vibration sources to three.  Cells are then
rendered using one of two methods: varying strength, or varying cadence.

_Varying intensity_ - The first half of a cell uses light pulses to mark empty
dots, and regular pulses to mark filled dots.  The second half of a cell uses
regular intensity pulses to mark empty dots, and heavy pulses to mark filled
dots.

_Varying cadence_ - Like the first method, light pulses mark empty dots, and
stronger pulses mark filled dots.  The pause duration between the first and
second half of the cells are timed at 2/3 the pause duration between cells.
Ex: If the pause between cells is set to 300ms, the pause between cell halves
would then be 200ms.
