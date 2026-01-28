# Custom Footprints Library

This directory contains custom KiCad footprint libraries (.kicad_mod files) for components used in the Fuse Power Distribution Board designs.

## Organization
- Group footprints by component type (e.g., fuses, connectors, etc.)
- Use clear, descriptive names
- Follow KiCad Library Convention (KLC) where possible

## Footprint Naming Convention
Format: `<Type>_<Description>_<Pitch/Size>`

Examples:
- `Fuse_Holder_5x20mm`
- `Connector_Terminal_2.54mm`
- `LED_0805`

## Creating Custom Footprints
1. Use KiCad Footprint Editor
2. Set appropriate courtyard clearances
3. Add 3D model associations
4. Include reference designator and value text
5. Test with actual components when possible

## Library Files
Custom footprint libraries should be saved as `.pretty` directories containing individual `.kicad_mod` files.

Example structure:
```
footprints/
  FusePowerDistribution.pretty/
    Fuse_Holder_5x20mm.kicad_mod
    Terminal_Block_2.54mm.kicad_mod
```

## Documentation
Document any special considerations or mounting requirements for custom footprints.
