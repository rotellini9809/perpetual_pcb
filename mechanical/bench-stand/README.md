# Bench stand

A 3D-printed stand that holds the Perpetual board still on the bench. Use it for IMU work: the
six-face calibration, and above all the arming gyroscope collection and the gyroscope-only tilt and
drift checks. Holding the board by hand during arming bakes a gyroscope bias into the attitude.

| File | Contents |
| --- | --- |
| [`perpetual-bench-stand.stl`](perpetual-bench-stand.stl) | Printable model, in mm (GitHub shows it in a 3D viewer) |

## Geometry

| Feature | Value |
| --- | --- |
| Base plate | 50 × 80 mm, 4 mm thick: the same outline as the board |
| Posts | 4, on the board's [mounting holes](../../README.md#mechanical): 3.5 mm from each edge, 43 × 73 mm apart |
| Post size | Ø5.5 mm, 7 mm tall: the board sits 7 mm above the plate, with room for the components on the back |
| Screw holes | Ø2.1 mm, 7 mm deep, blind: pilot holes for M2.5 screws |

## Printing and assembly

Print it flat, with the base plate on the bed; the posts need no supports.

Fix the board with four **M2.5 screws, 6–8 mm long**, threaded directly into the pilot holes. The
board is 1.6 mm thick, so an 8 mm screw goes about 6.4 mm into a 7 mm hole. Do not overtighten
the screws in plastic.
