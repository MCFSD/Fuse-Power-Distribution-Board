# Component Libraries

This directory contains custom libraries for the Fuse Power Distribution Board project.

## Subdirectories

### symbols/
Custom KiCad symbol libraries for components used in the boards. These are schematic symbols specific to this project and may not be available in the standard KiCad libraries.

### footprints/
Custom KiCad footprints for components used in the boards. These footprints are specific to this project and may not be available in the standard KiCad libraries.

### 3d-models/
3D models for components in STEP (.step) or WRL (.wrl) format. These models are used for 3D visualization and mechanical validation of the PCB designs.

## Using Custom Libraries

### In KiCad 9.0+
1. Open KiCad project
2. Go to Preferences → Manage Symbol Libraries
3. Add the symbols directory as a library path
4. Go to Preferences → Manage Footprint Libraries
5. Add the footprints directory as a library path
6. Go to Preferences → Configure Paths
7. Set up path variables for 3D models directory

## Library Organization
- Use descriptive names for footprints and models
- Include documentation for custom components
- Keep models in appropriate formats (STEP preferred)
- Maintain consistency across all board designs

## Contributing
When adding new components:
1. Document the component in the library README
2. Include datasheets if applicable
3. Test footprints before committing
4. Ensure 3D models are properly aligned
