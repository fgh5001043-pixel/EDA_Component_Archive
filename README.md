# EDA_Component_Archive

Private raw-source archive for Auto EE EDA validation.

## Purpose

This repository stores original component packages and supporting source material so validation work can reference GitHub directly instead of repeatedly uploading files into chat.

## Upload workflow

For the fastest workflow, upload each component as a single ZIP file under `components/` and name the ZIP with the manufacturer part number.

Examples:

- `components/LMG1020.zip`
- `components/CSD95496QVM.zip`
- `components/5747844-4.zip`

A ZIP may contain any source material relevant to that component, including:

- Datasheets / product drawings
- KiCad symbol and footprint files
- Cadence / OrCAD / Allegro exports
- Altium files or screenshots
- Gerber / STEP / 3D files
- Validation screenshots
- Notes or result files

## Naming rule

Use the exact manufacturer part number whenever possible. Keep one component per ZIP.

Preferred format:

`components/<MPN>.zip`

If more than one package is needed for the same component, append a clear suffix, for example:

- `LMG1020-source.zip`
- `LMG1020-altium.zip`
- `LMG1020-gerber.zip`

## Validation status

Validation results may use the following status vocabulary:

- `PASS` — checked and consistent with the datasheet / expected EDA mapping
- `PARTIAL` — some items checked, but validation is incomplete
- `FAIL` — a confirmed inconsistency or defect was found
- `NOT CHECKED` — not yet verified

## Relationship to EDA_Native_Validator

`EDA_Component_Archive` is the source-data archive. `EDA_Native_Validator` remains the validator/tooling repository. Keep raw component packages here rather than mixing them into the validator codebase.
