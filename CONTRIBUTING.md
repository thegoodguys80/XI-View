# Contributing to XI-View

Thank you for your interest in contributing to XI-View! This document provides guidelines for contributing icon modifications, bug fixes, and improvements to this Final Fantasy XI UI enhancement mod.

## Table of Contents
- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Contribution Types](#contribution-types)
- [Development Guidelines](#development-guidelines)
- [Pull Request Process](#pull-request-process)
- [Community](#community)

## Code of Conduct

### Our Standards
- Be respectful and inclusive
- Provide constructive feedback
- Focus on what's best for the community
- Show empathy towards other contributors

### Unacceptable Behavior
- Harassment or discriminatory language
- Trolling or insulting comments
- Publishing others' private information
- Other conduct inappropriate for a professional setting

## Getting Started

### Prerequisites
- **Operating System**: Windows (FFXI is Windows-only)
- **FFXI Installation**: Active Final Fantasy XI installation
- **Git**: For version control
- **Tools**: 
  - ChangeTex (included in `03 - Utilities/`)
  - FFXI Icon Change (included in `03 - Utilities/`)
  - gc3_Graphics editor (included in `03 - Utilities/`)

### Fork and Clone
1. Fork the repository on GitHub
2. Clone your fork locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/XI-View.git
   cd XI-View
   ```
3. Add upstream remote:
   ```bash
   git remote add upstream https://github.com/thegoodguys80/XI-View.git
   ```
4. Keep your fork synced:
   ```bash
   git fetch upstream
   git checkout master
   git merge upstream/master
   ```

### Create a Backup
**CRITICAL**: Always backup your FFXI ROM files before making changes:
```bash
# Backup your current FFXI ROM folder
cp -r "C:\Program Files\PlayOnline\SquareEnix\FINAL FANTASY XI\ROM" "C:\FFXI_Backup\ROM_$(date +%Y%m%d)"
```

Or use the included backups in `00 - Original Backup/ROM/`.

## How to Contribute

### Reporting Bugs
Use the [GitHub Issues](https://github.com/thegoodguys80/XI-View/issues) page to report bugs.

**Bug Report Template**:
```markdown
**Description**: Brief description of the issue

**FFXI Version**: (e.g., June 2025, April 2025)

**Steps to Reproduce**:
1. Install XI-View version X
2. Start FFXI
3. Observe issue at [location]

**Expected Behavior**: What should happen

**Actual Behavior**: What actually happens

**Screenshots**: If applicable

**Installation Method**: (e.g., Manual copy, ChangeTex)

**Affected Files**: Which ROM files were modified
```

### Suggesting Features
Feature requests are welcome! Please:
- Check if the feature has already been requested
- Clearly describe the feature and its benefits
- Explain how it fits with FFXI's UI limitations
- Consider implementation complexity

### Security Vulnerabilities
**DO NOT** file public issues for security vulnerabilities. See [SECURITY.md](SECURITY.md) for responsible disclosure guidelines.

## Contribution Types

### 1. Icon Modifications

#### Creating New Icons
1. Extract original icon from FFXI ROM using extraction tool (see [TOOLS.md](docs/TOOLS.md))
2. Edit icon in graphics editor (must be same dimensions)
3. Test in-game to verify it displays correctly
4. Document the icon ID and purpose

#### Modifying Existing Icons
1. Locate the icon in the appropriate ROM folder
2. Make modifications using gc3_Graphics or similar tool
3. Preserve original dimensions and format
4. Test thoroughly in-game

#### Icon Quality Guidelines
- **Format**: Must match original icon format (.DAT file)
- **Dimensions**: Must match exactly (no scaling)
- **Color Depth**: Maintain original color depth
- **Transparency**: Preserve alpha channels
- **Consistency**: Match FFXI's visual style

### 2. Version Updates

When FFXI releases a new version:
1. Test current XI-View icons with new FFXI version
2. Document any issues in [VERSION.md](VERSION.md)
3. Fix broken icons (e.g., June 2025 Limbus icons - Issue #41)
4. Update compatibility matrix in VERSION.md
5. Create release notes

### 3. Documentation

Documentation improvements are always welcome:
- Fix typos or unclear instructions
- Add screenshots or video guides
- Improve installation steps
- Document utility usage
- Expand icon index

### 4. Utilities and Tools

Contributions to improve or replace utilities:
- Python scripts for automation
- Icon extraction tools
- Installation validators
- Backup utilities

**Note**: See P3-001 in BACKLOG.md for open-source utility rewrite initiative.

### 5. Testing and Validation

Help test and validate changes:
- Test on different FFXI versions
- Verify checksums match
- Report compatibility issues
- Test installation procedures

## Development Guidelines

### File Organization

```
XI-View/
├── 00 - Original Backup/ROM/        # Never modify - reference only
├── 01 - Normal Screen [4x3]/ROM/    # 4:3 aspect ratio icons
├── 02 - Widescreen [16x9]/ROM/      # 16:9 aspect ratio icons
├── 03 - Utilities/                  # Helper tools
├── 04 - Other/                      # Miscellaneous files
├── 05 - Add Ons/                    # Additional modifications
├── docs/                            # Documentation (future)
├── tests/                           # Test scripts (future)
└── README.md
```

### Branch Naming Conventions

Use descriptive branch names:
- **Feature**: `feature/icon-limbus-june2025`
- **Bugfix**: `fix/icon-transparency-issue`
- **Documentation**: `docs/improve-readme`
- **Refactor**: `refactor/reorganize-folders`

### Commit Message Format

Follow conventional commits:
```
<type>(<scope>): <subject>

[optional body]

[optional footer]
```

**Types**:
- `feat`: New feature (e.g., new icon set)
- `fix`: Bug fix (e.g., broken icon)
- `docs`: Documentation changes
- `refactor`: Code refactoring
- `test`: Adding tests
- `chore`: Maintenance tasks

**Examples**:
```bash
feat(icons): Add June 2025 Limbus icons

- Fixed "DEBUG" placeholder issue
- Updated 12 Limbus buff icons
- Tested with FFXI version 2.0

Fixes #41
```

```bash
docs: Update README with visual installation guide

- Added before/after screenshots
- Clarified backup procedure
- Fixed broken video link
```

### Testing Requirements

Before submitting a pull request:

1. **Visual Testing**
   - Launch FFXI with modified icons
   - Verify icons display correctly in-game
   - Check both 4:3 and 16:9 versions (if applicable)
   - Test in relevant game scenarios (e.g., Limbus for buff icons)

2. **File Integrity**
   - Verify file sizes match expectations
   - Check that ROM files are not corrupted
   - Ensure backups can restore original state

3. **Compatibility**
   - Test on current FFXI version
   - Document if changes are version-specific
   - Update VERSION.md if compatibility changes

4. **Checksums**
   - Update CHECKSUMS.txt for any modified files
   - Verify SHA-256 hashes are correct

### Code Quality

For Python/scripting contributions:
- Follow PEP 8 style guide (Python)
- Add docstrings to functions
- Include error handling
- Add comments for complex logic
- Write tests when possible

## Pull Request Process

### 1. Prepare Your Changes

```bash
# Create feature branch
git checkout -b feature/your-feature-name

# Make changes and commit
git add .
git commit -m "feat(scope): your changes"

# Push to your fork
git push origin feature/your-feature-name
```

### 2. Create Pull Request

1. Go to your fork on GitHub
2. Click "New Pull Request"
3. Select your feature branch
4. Fill out the PR template:

**PR Template**:
```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Refactoring
- [ ] Other (specify)

## Changes Made
- List of specific changes
- Files modified
- Icons added/updated

## Testing
- [ ] Tested in FFXI (version: ___)
- [ ] Verified checksums
- [ ] Tested backup/restore
- [ ] Updated VERSION.md (if applicable)

## Screenshots
[Add screenshots if applicable]

## Related Issues
Fixes #XX
Related to #YY

## Checklist
- [ ] My code follows the style guidelines
- [ ] I have updated documentation
- [ ] I have added/updated tests
- [ ] All tests pass
- [ ] I have updated CHECKSUMS.txt
- [ ] I have backed up original files
```

### 3. Code Review

Your PR will be reviewed for:
- **Functionality**: Does it work as intended?
- **Quality**: Is the code/modification clean?
- **Testing**: Has it been tested in-game?
- **Documentation**: Are changes documented?
- **Compatibility**: Does it maintain FFXI version compatibility?

### 4. Address Feedback

- Respond to review comments
- Make requested changes
- Push updates to your branch
- Re-request review when ready

### 5. Merge

Once approved:
- PR will be merged by a maintainer
- Your branch can be deleted
- Changes will appear in the next release

## Development Setup

### Recommended Tools

1. **FFXI ROM Editor**: gc3_Graphics (included)
2. **Texture Tool**: ChangeTex (included)
3. **Icon Manager**: FFXI Icon Change (included)
4. **Text Editor**: VS Code, Sublime Text, or similar
5. **Graphics Editor**: GIMP, Photoshop, or similar (for icon design)
6. **Hex Editor**: HxD or similar (for advanced DAT editing)

### Directory Structure

Keep your workspace organized:
```
~/FFXI_Dev/
├── XI-View/                 # Your fork
├── FFXI_Backup/             # Your FFXI backups
├── FFXI_Test/               # Test FFXI installation (optional)
└── tools/                   # Additional tools
```

## Style Guide

### Documentation
- Use clear, concise language
- Add code examples where helpful
- Include screenshots for visual steps
- Update table of contents when adding sections

### File Naming
- Use descriptive names
- Follow existing naming patterns
- Avoid spaces (use hyphens or underscores)
- Include version info when relevant

### Comments
- Explain why, not what
- Document complex logic
- Include icon IDs and descriptions
- Add TODOs for future improvements

## Community

### Getting Help
- **GitHub Issues**: Ask questions, report bugs
- **Discussions**: General discussion (if enabled)
- **Discord**: [Link if available]
- **Reddit**: r/ffxi community

### Staying Updated
- Watch the repository for notifications
- Follow release notes
- Check VERSION.md for compatibility updates
- Subscribe to issue notifications

### Recognition

Contributors are recognized in:
- Release notes (CHANGELOG.md)
- README.md contributors section
- Commit history
- Issue/PR acknowledgments

## License

By contributing, you agree that your contributions will be licensed under the same MIT License that covers the project. See [LICENSE](LICENSE) for details.

## Additional Resources

- [README.md](README.md) - Project overview and installation
- [VERSION.md](VERSION.md) - FFXI version compatibility
- [SECURITY.md](SECURITY.md) - Security policies
- [CHECKSUMS.txt](CHECKSUMS.txt) - File verification
- [TOOLS.md](docs/TOOLS.md) - Utility documentation (coming soon)
- [BACKLOG.md](docs/BACKLOG.md) - Planned improvements

## Questions?

If you have questions not covered here:
1. Check existing documentation
2. Search closed issues
3. Open a new issue with the `question` label
4. Be specific and include context

---

**Thank you for contributing to XI-View!**

Your contributions help improve the FFXI experience for players worldwide.

---

**Last Updated**: January 16, 2026  
**Maintained By**: thegoodguys80  
**Original Project**: Caradog/XI-View