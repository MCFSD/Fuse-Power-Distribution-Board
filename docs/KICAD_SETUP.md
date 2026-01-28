# KiCad Project Setup Guide

This guide explains how to create and set up KiCad projects for the Fuse Power Distribution Boards.

## Prerequisites
- KiCad 9.0 or higher installed
- This repository cloned locally
- Custom libraries configured (see main README.md)

## Creating a New Board Design

### Step 1: Create KiCad Project
1. Open KiCad
2. Create a new project in the appropriate board directory
3. Name the project using the format: `<Voltage>-FusePowerDistribution`
   - Example: `48V-FusePowerDistribution.kicad_pro`

### Step 2: Configure Project Settings
1. Open Project Manager
2. Set up design rules appropriate for the voltage level
3. Configure netclasses for power distribution
4. Set appropriate trace widths for current requirements

### Step 3: Set Up Libraries
1. **Symbol Libraries**: Use standard KiCad libraries plus custom symbols
2. **Footprint Libraries**: Add path to `libraries/footprints/`
3. **3D Models**: Configure path to `libraries/3d-models/`

### Step 4: Schematic Design
1. Create hierarchical sheets if needed
2. Use clear net names (e.g., VIN, VOUT1, VOUT2)
3. Include proper decoupling
4. Add fuse protection for all outputs
5. Include status LEDs and test points

### Step 5: PCB Layout
1. Define board outline and mounting holes
2. Place connectors on board edges
3. Route power traces with appropriate widths
4. Add copper pours for ground and power planes
5. Include silkscreen labels for all connectors

### Step 6: Design Validation
1. Run Electrical Rules Check (ERC) on schematic
2. Run Design Rules Check (DRC) on PCB
3. Check 3D view for mechanical clearances
4. Review BOM for component availability

### Step 7: Documentation
1. Generate BOM from schematic
2. Export schematic PDF
3. Create assembly drawing
4. Update version history

## Design Considerations by Voltage

### 48V Board
- Higher voltage isolation requirements
- Appropriate creepage and clearance distances
- Consider using optoisolators for control signals
- Heavy copper for high current paths

### 24V Board
- Common industrial voltage
- Moderate current handling
- Standard PCB materials adequate

### 12V Board
- Automotive applications common
- May require higher current capacity
- Consider reverse polarity protection

### 5V Board
- Most common for digital circuits
- May handle high currents despite low voltage
- USB power considerations if applicable

## File Organization

After creating the project, ensure the following files exist:
```
boards/<voltage>/
  ├── <voltage>-FusePowerDistribution.kicad_pro    # Project file
  ├── <voltage>-FusePowerDistribution.kicad_sch    # Schematic
  ├── <voltage>-FusePowerDistribution.kicad_pcb    # PCB layout
  ├── README.md                                     # Board-specific docs
  └── datasheets/                                   # Component datasheets (optional)
```

## Best Practices
- Save frequently
- Use version control (commit after major milestones)
- Keep backups (KiCad creates automatic backups)
- Test designs before manufacturing
- Document design decisions
- Update BOM when adding/removing components

## Common Components
Typical components for fuse distribution boards:
- **Fuses**: Blade fuses, cartridge fuses (select based on voltage/current)
- **Fuse holders**: PCB mount or panel mount
- **Connectors**: Screw terminals, Molex, or appropriate power connectors
- **LEDs**: Status indicators (with current limiting resistors)
- **TVS Diodes**: Transient voltage suppression (optional)
- **Capacitors**: Input/output filtering

## Testing Checklist
Before finalizing a design:
- [ ] ERC passes with no errors
- [ ] DRC passes with no errors
- [ ] All footprints have 3D models
- [ ] Trace widths appropriate for current
- [ ] Clearances meet voltage requirements
- [ ] All components are available/in stock
- [ ] BOM is complete and accurate
- [ ] Silkscreen is readable
- [ ] Version number is updated
- [ ] Changes are documented
