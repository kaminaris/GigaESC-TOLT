# Local libraries

Custom dependencies are contained in this project; standard KiCad 10 libraries and 3D models are still required.

- `GigaTOLTSymbols.kicad_sym`: nine cached custom symbol definitions used by the project schematic files, including retained inactive sheets. The different +3.3REF definitions are preserved as separate variants.
- `GigaTOLTLibrary.pretty`: eight additional footprint definitions, copied from the placed PCB where available and from the individual source footprint otherwise. Existing local footprints are retained.
- `3DModels`: the three referenced custom driver, current-sensor and capacitor models. Standard and already embedded models remain unchanged.
- Library tables use `${KIPRJMOD}` paths; the external GigaVesc library entries were removed.

## Interface review — 2026-09-26

The compact symbols and their stacked supply/ground pins retain all 90 unique electrical pin identifiers and match their PCB pad nets. Library symbols match the schematic copies. The intentional CAN swap is retained: J33_14 carries IN-CANH and J33_16 carries IN-CANL. Their symbol pin names still describe the original mapping, so consult the connected net labels.

Localization preserves schematic net connectivity and PCB pad positions, sizes and nets. All 480 existing tracks/vias remain. The preliminary PCB DRC still reports 322 unconnected items and numerous shorts/clearance violations; this is not a manufacturing sign-off.
