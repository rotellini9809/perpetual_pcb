Waveshare RP2350-Tiny complete KiCad library
============================================

Contents
--------
Waveshare_RP2350_Tiny.kicad_sym
    Complete 36-physical-pin schematic symbol.

Waveshare_RP2350_Tiny_AllPads.pretty/
    Waveshare_RP2350_Tiny_AllPads_36Pin.kicad_mod
    Complete carrier footprint with all edge, underside GPIO/power and SWD pads.

RP2350_Tiny_36Pin_Map.csv
    Full symbol-to-footprint pin map.

symbol_preview.svg
    Human-readable preview of the symbol layout.

Numbering strategy
------------------
Pins 1–23 preserve the edge-only model numbering:
  1–16  = GP0–GP15
  17–20 = GP26/ADC0 through GP29/ADC3
  21    = 3V3 edge contact
  22    = GND edge contact
  23    = VSYS / board pad marked 5V

Added underside contacts:
  24 = 3V3
  25 = GP23
  26 = GP22
  27 = GP21
  28 = GP20

  29 = GND
  30 = GP16 / onboard WS2812 RGB input
  31 = GP17
  32 = GP18
  33 = GP19

  34 = SWCLK
  35 = GND
  36 = SWDIO

All 36 physical contacts are separate symbol pins. This means the two 3V3
lands and the three GND lands are explicitly represented and can be checked
by ERC and during PCB inspection.

Not included
------------
GP24 and GP25 are used by resistor/configuration circuitry on the module and
are not exposed as normal carrier-board solder contacts.

The onboard FPC connector signals are not represented as carrier pads because
the connector is already fitted to the RP2350-Tiny module.

Install
-------
1. In KiCad: Preferences -> Manage Symbol Libraries.
2. Add Waveshare_RP2350_Tiny.kicad_sym.
3. In Preferences -> Manage Footprint Libraries.
4. Add the Waveshare_RP2350_Tiny_AllPads.pretty directory.
5. Use the library nickname "Waveshare_RP2350_Tiny_AllPads" so the symbol's
   pre-assigned footprint field resolves automatically.

Compatibility
-------------
The symbol uses the KiCad 8 modern symbol format and is intended to open in
KiCad 8, 9 and 10. The footprint uses the modern .kicad_mod format.

Manufacturing warning
---------------------
The underside pad locations were reconstructed from Waveshare's published
mechanical drawing. Waveshare does not publish an official KiCad carrier
land-pattern recommendation. Before ordering:
  - Print the footprint at 1:1.
  - Place the real module over it.
  - Verify all 13 underside contacts.
  - Verify the FPC/top orientation.
  - Reduce underside paste apertures if reflowing, to reduce module float.
