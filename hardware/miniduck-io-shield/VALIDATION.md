# Validation record

The source snapshot was checked and regenerated with KiCad CLI 9.0.4 on 2026-08-26. These results document the existing fabricated prototype; they do not replace an engineering review.

## Export results

- Schematic PDF: generated successfully.
- BOM: generated successfully.
- Top and bottom 3D renders: generated successfully.
- Gerber and PTH/NPTH drill outputs: generated successfully.

## ERC

- Error-severity items: 0
- Warning-severity items: 35
- All 35 warnings are `unconnected_wire_endpoint` items in the schematic.

Review each endpoint in KiCad before editing or reusing the circuit. The warnings are retained in [`docs/erc-report.json`](docs/erc-report.json).

## PCB DRC

- Error-severity items: 0
- Warning-severity items: 12
- Unconnected PCB items: 0
- Schematic-parity warnings: 2

The 12 PCB warnings consist of:

- 2 silkscreen-to-board-edge clearance warnings near J13.
- 2 placed-footprint/library-copy mismatch warnings for J5 and the Raspberry Pi reference footprint.
- 6 minimum silkscreen text-height warnings.
- 2 silkscreen-over-solder-mask warnings around J5.

The two schematic-parity warnings are extra mechanical/reference footprints without normal schematic components. Full machine-readable details are retained in [`docs/drc-report.json`](docs/drc-report.json).

## Known design-review items

1. Correct the J9/J10/J14 LED silkscreen labels or the connector/net assignment so physical labels and electrical functions agree.
2. Change R1's footprint library assignment from the capacitor library to the matching 0603 resistor footprint.
3. Resolve or intentionally exclude the ERC wire-endpoint warnings.
4. Review the J13 silkscreen/edge clearance and all small silkscreen text against the selected PCB vendor's rules.
5. Confirm the custom SW1 footprint and the physical orientation of every polarized/pin-1 component before ordering.
