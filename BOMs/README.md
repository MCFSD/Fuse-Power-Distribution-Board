# Bill of Materials (BOM)

This directory contains the Bill of Materials (BOM) for each power distribution board variant.

## Files
- **48V-BOM.csv** - BOM for 48V board
- **24V-BOM.csv** - BOM for 24V board
- **12V-BOM.csv** - BOM for 12V board
- **5V-BOM.csv** - BOM for 5V board

## Format
Each BOM file is in CSV format with the following columns:
- **Reference**: Component reference designator (e.g., F1, C1, R1)
- **Quantity**: Number of this component needed
- **Value**: Component value (e.g., resistance, capacitance, fuse rating)
- **Footprint**: PCB footprint name
- **Datasheet**: Link to component datasheet
- **Manufacturer**: Component manufacturer name
- **Manufacturer Part Number**: Manufacturer's part number
- **Supplier**: Where to purchase the component
- **Supplier Part Number**: Supplier's part number
- **Notes**: Additional notes or comments

## Updating BOMs
BOMs can be automatically generated from KiCad using the built-in BOM generation tools. Update these files whenever the schematic changes.
