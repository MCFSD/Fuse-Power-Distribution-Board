# Custom Symbols Library

This directory contains custom KiCad symbol libraries (.kicad_sym files) for components used in the Fuse Power Distribution Board designs.

## Organization
- Group symbols by component type or function
- Use clear, descriptive names
- Follow KiCad Library Convention (KLC) where possible

## Symbol Naming Convention
Format: `<Type>_<Description>`

Examples:
- `Fuse_BladeFuse_ATO`
- `Connector_PowerTerminal_2Pin`
- `LED_Status_Indicator`

## Creating Custom Symbols
1. Use KiCad Symbol Editor
2. Define appropriate pin types (power input, output, etc.)
3. Add reference designator prefix
4. Include datasheet link in symbol properties
5. Set appropriate default footprint associations

## Library Files
Custom symbol libraries should be saved as `.kicad_sym` files.

Example structure:
```
symbols/
  FusePowerDistribution.kicad_sym
```

## Adding to KiCad
1. Open KiCad
2. Go to **Preferences → Manage Symbol Libraries**
3. Add the `libraries/symbols/` directory
4. Select the appropriate library file

## Symbol Requirements
- Pin names should match datasheet
- Power pins should be properly designated
- Include all necessary pins
- Set appropriate electrical types (input, output, power, etc.)
- Add symbol to appropriate library file

## Documentation
Document any custom symbols or special usage notes. Include references to datasheets for custom components.
