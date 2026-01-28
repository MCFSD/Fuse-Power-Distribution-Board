# Contributing Guidelines

Thank you for your interest in contributing to the Fuse Power Distribution Board project!

## How to Contribute

### Reporting Issues
- Use GitHub Issues to report bugs or suggest enhancements
- Provide clear description of the issue
- Include steps to reproduce (if applicable)
- Specify which board variant is affected

### Making Changes

#### 1. Fork and Clone
```bash
git clone https://github.com/MCFSD/Fuse-Power-Distribution-Board.git
cd Fuse-Power-Distribution-Board
```

#### 2. Create a Branch
```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/your-bug-fix
```

Branch naming conventions:
- `feature/` - New features or enhancements
- `fix/` - Bug fixes
- `docs/` - Documentation updates
- `refactor/` - Code refactoring

#### 3. Make Your Changes
- Follow the design guidelines in README.md
- Update documentation as needed
- Test your changes thoroughly
- Run KiCad ERC and DRC checks

#### 4. Update Documentation
When making changes:
- Update the appropriate BOM file if components change
- Update `docs/versions/CHANGELOG.md`
- Update board-specific version history
- Add comments to explain design decisions

#### 5. Commit Your Changes
Use clear, descriptive commit messages:
```bash
git add .
git commit -m "Add fuse selection for 48V board output channels"
```

Commit message format:
- Start with a verb (Add, Fix, Update, Remove)
- Be specific and concise
- Reference issue numbers if applicable (#123)

#### 6. Push and Create Pull Request
```bash
git push origin your-branch-name
```
Then create a Pull Request on GitHub.

## Design Standards

### Schematic Design
- Use hierarchical design for complex schematics
- Label all nets clearly
- Include power flags where appropriate
- Add documentation text for important notes
- Follow KiCad best practices

### PCB Layout
- Maintain appropriate trace widths for current
- Use copper pours for ground planes
- Include mounting holes in standardized positions
- Label all connectors on silkscreen
- Keep high-current traces short and direct
- Maintain proper clearances for voltage levels

### Component Selection
- Prefer readily available components
- Document any specialty components
- Include alternate part numbers when possible
- Consider lead times and lifecycle status
- Verify component footprints before use

### Library Components
When adding custom symbols, footprints, or 3D models:
- Follow KiCad Library Convention (KLC)
- Use descriptive names
- Include proper documentation
- Test with actual components if possible
- Add to appropriate library directory (symbols/, footprints/, or 3d-models/)

## Code Review Process

All contributions will be reviewed for:
1. Design correctness (ERC/DRC clean)
2. Documentation completeness
3. BOM accuracy
4. Appropriate component selection
5. Compliance with design standards

## Version Control

### Semantic Versioning
Follow semantic versioning for all boards:
- **MAJOR.MINOR.PATCH**
- MAJOR: Breaking changes or redesign
- MINOR: New features, backward compatible
- PATCH: Bug fixes, minor improvements

### Git Tags
Tag releases with format:
```bash
git tag -a 48V-v1.0.0 -m "48V board version 1.0.0"
git push origin 48V-v1.0.0
```

### Commit Frequency
- Commit logical units of work
- Don't commit broken designs
- Include all related files in commits
- Ensure ERC/DRC pass before committing

## File Management

### What to Commit
✅ Commit these files:
- `.kicad_pro` - Project files
- `.kicad_sch` - Schematic files
- `.kicad_pcb` - PCB layout files
- `.csv` - BOM files
- `.md` - Documentation
- Custom libraries (symbols, footprints)
- 3D models (if reasonable size)

### What NOT to Commit
❌ Don't commit:
- Backup files (`*-bak`, `*.bck`)
- Auto-generated cache files
- Build outputs (gerbers unless specifically needed)
- Temporary files
- OS-specific files (.DS_Store, Thumbs.db)

The `.gitignore` file is configured to exclude these automatically.

## Testing and Validation

Before submitting a pull request:
- [ ] Run ERC on all modified schematics
- [ ] Run DRC on all modified PCB layouts
- [ ] Verify all footprints exist and are correct
- [ ] Check 3D view for mechanical issues
- [ ] Update BOM if components changed
- [ ] Update documentation
- [ ] Test file compatibility with KiCad 9.0+

## Questions?

If you have questions about contributing:
- Open an issue for discussion
- Contact the project maintainers
- Check existing documentation

## License

By contributing, you agree that your contributions will be licensed under the same license as the project.

---

Thank you for contributing to the Fuse Power Distribution Board project!
