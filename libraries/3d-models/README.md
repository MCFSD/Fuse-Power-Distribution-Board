# 3D Models Library

This directory contains 3D models for components used in the Fuse Power Distribution Board designs.

## Supported Formats
- **STEP (.step, .stp)**: Preferred format for mechanical validation
- **WRL (.wrl)**: VRML format for KiCad 3D viewer

## Organization
Organize models by component type or manufacturer:
```
3d-models/
  fuses/
  connectors/
  capacitors/
  resistors/
```

## Model Naming Convention
Use descriptive names that match the component:
- `Fuse_Littelfuse_5x20mm.step`
- `Terminal_Block_Phoenix_2.54mm.wrl`

## Sourcing 3D Models
1. Manufacturer websites (preferred)
2. Component distributor sites (Digi-Key, Mouser)
3. 3D model libraries (GrabCAD, KiCad library)
4. Create custom models if needed

## Model Requirements
- Properly oriented (Z-axis up)
- Correct scale (1:1)
- Centered on origin or pin 1
- Simplified geometry for performance

## Linking Models to Footprints
In KiCad Footprint Editor:
1. Open the footprint
2. Go to Footprint Properties → 3D Settings
3. Add the model file path
4. Adjust offset, rotation, and scale as needed

## File Size Considerations
- Keep models reasonably detailed but not overly complex
- Use simplified geometry for better performance
- Consider file size when committing to repository
