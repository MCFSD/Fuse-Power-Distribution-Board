# Fuse Power Distribution Board

A comprehensive repository for storing and managing fuse power distribution circuit board designs, including KiCad project files, BOMs, libraries, and version history.

## Overview

This repository contains designs for four different voltage variants of fuse power distribution boards:
- **48V** - 48 Volt power distribution board
- **24V** - 24 Volt power distribution board  
- **12V** - 12 Volt power distribution board
- **5V** - 5 Volt power distribution board

Each board provides fused power distribution with appropriate protection and current ratings for its voltage level.

## Repository Structure

```
├── boards/              # KiCad project files for each board variant
│   ├── 48V/            # 48V board design
│   ├── 24V/            # 24V board design
│   ├── 12V/            # 12V board design
│   └── 5V/             # 5V board design
├── BOMs/               # Bill of Materials for each board
│   ├── 48V-BOM.csv
│   ├── 24V-BOM.csv
│   ├── 12V-BOM.csv
│   └── 5V-BOM.csv
├── libraries/          # Custom component libraries
│   ├── footprints/    # Custom KiCad footprints
│   └── 3d-models/     # 3D models for components
└── docs/              # Documentation
    └── versions/      # Version history and changelog
```

## Requirements

- **KiCad**: Version 9.0 or higher
- All boards are designed using KiCad EDA software

## Getting Started

### Cloning the Repository
```bash
git clone https://github.com/MCFSD/Fuse-Power-Distribution-Board.git
cd Fuse-Power-Distribution-Board
```

### Opening a Board Design
1. Navigate to the appropriate board directory (e.g., `boards/48V/`)
2. Open the `.kicad_pro` file in KiCad
3. Configure library paths if needed (see Libraries section)

### Setting Up Custom Libraries
1. Open KiCad
2. Go to **Preferences → Manage Footprint Libraries**
3. Add the `libraries/footprints/` directory
4. Go to **Preferences → Configure Paths**
5. Set up path variables for `libraries/3d-models/`

## Bill of Materials (BOMs)

Each board has a corresponding BOM file in CSV format located in the `BOMs/` directory. These files contain:
- Component references and quantities
- Part values and footprints
- Manufacturer and supplier information
- Datasheets and notes

BOMs can be automatically generated from KiCad schematics and should be updated whenever the design changes.

## Version Control and History

### Versioning Strategy
This project uses semantic versioning (MAJOR.MINOR.PATCH):
- **MAJOR**: Incompatible changes or complete redesign
- **MINOR**: New features in a backward-compatible manner
- **PATCH**: Backward-compatible bug fixes

### Git Workflow
- Use branches for development work
- Tag releases with version numbers (e.g., `48V-v1.0.0`)
- Document all changes in `docs/versions/CHANGELOG.md`
- Maintain individual version history files for each board

### Tracking Changes
- See `docs/versions/CHANGELOG.md` for consolidated changes
- See `docs/versions/<voltage>-versions.md` for board-specific history
- Use git tags to mark official releases

## Contributing

When making changes to any board design:

1. **Create a branch** for your work
2. **Update the schematic** and/or PCB layout
3. **Update the BOM** if components change
4. **Document changes** in the appropriate version history file
5. **Test the design** (DRC, ERC checks in KiCad)
6. **Commit changes** with clear commit messages
7. **Update version numbers** following semantic versioning

## Design Guidelines

- Follow KiCad Library Convention (KLC) for custom components
- Use descriptive reference designators
- Include proper clearances and design rules
- Document any design decisions or special considerations
- Run Design Rule Check (DRC) and Electrical Rule Check (ERC) before committing

## Manufacturing

For manufacturing files (Gerbers, drill files, etc.):
- Generate files using KiCad's Plot function
- Include a README with manufacturing notes
- Specify PCB stackup and materials
- Include assembly drawings if needed

## License

Please specify the license for this project.

## Contact

For questions or issues, please contact the project maintainers or open an issue in this repository.

---

**Project Status**: Initial Setup Complete  
**Last Updated**: January 2026  
**KiCad Version**: 9.0+
