# Changelog

All notable changes to XI-View will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- SECURITY.md with vulnerability disclosure policy
- CONTRIBUTING.md with comprehensive contribution guidelines
- LICENSE file (MIT)
- CHECKSUMS.txt with SHA-256 file verification
- VERSION.md with FFXI compatibility matrix
- STATUS.md project dashboard

### Changed
- Improved documentation structure
- Enhanced security posture

## [2.0] - 2025-06-XX (June 2025 Update)

### Known Issues
- **CRITICAL**: Limbus buff icons display as "DEBUG" placeholder (Issue #41)
- Issue affects June 2025 FFXI version
- Workaround: Use April 2025 icons temporarily

### Added
- Updated icons for June 2025 FFXI version
- Compatibility with FFXI version 2.0

### Changed
- Icons updated to match June 2025 game version
- Status icon compatibility maintained

### Fixed
- Various icon compatibility issues

## [2.0] - 2025-04-XX (April 2025 Update)

### Added
- Updated icons for April 2025 FFXI version
- New status icons for recent game additions

### Changed
- Icons refreshed for current FFXI content

## [2.0] - 2024-06-XX (June 2024 Update)

### Added
- Updated status icons for June 2024 FFXI version
- Compatibility fixes for mid-2024 game updates

## [2.0] - 2024-05-XX (May 2024 Update)

### Added
- Updated icons for May 2024 FFXI version

## [2.0] - 2023-11-XX (November 2023 Update)

### Added
- Updated status icons for November 2023 FFXI version

## [2.0] - 2023-02-XX (February 2023 Update)

### Added
- Updated icons for February 2023 FFXI version

## [2.0.21] - 2022-02-XX (February 2022 Update)

### Added
- Updated status icons for February 2022 FFXI version

## [2.0.19] - 2021-11-10 (November 10th 2021 Update)

### Added
- Updated icons for November 2021 FFXI version
- Compatibility with late 2021 game updates

## [2.0.18] - 2020-11-XX (November 2020 Update)

### Added
- Updated icons for November 2020 FFXI version
- New status icon designs

## [2.0.18] - 2020-10-XX (October 2020 Update)

### Added
- Updated status icons for October 2020 FFXI version
- DDS image files for texture modifications

## [2.0.18] - 2020-08-XX (August 2020 Update)

### Added
- Updated icons for August 2020 FFXI version

## [2.0] - 2020-04-03 (April 3rd 2020 Update)

### Added
- Updated status icons for April 2020 FFXI version

## [2.0] - 2020-02-XX (February 2020 Update)

### Added
- Updated icons for February 2020 FFXI version

## [2.0] - 2019-12-XX (December 2019 Update)

### Added
- Updated status icons for December 2019 FFXI version

## [2.0] - 2019-11-XX (November 2019 Update)

### Added
- Updated icons for November 2019 FFXI version

## [2.0.9] - 2019-10-XX (October 2019 Update)

### Added
- Updated status icons for October 2019 FFXI version
- Version milestone: v2.0.9

## [2.0] - 2019-05-XX (May 2019 Update)

### Added
- Updated icons for May 2019 FFXI version

## [2.0.6] - 2018-05-XX (May 2018 Update)

### Added
- Updated status icons for May 2018 FFXI version
- Compatibility improvements

## [2.0.5] - 2017-XX-XX

### Added
- Updated icons and compatibility fixes
- Improved status icon clarity

## [2.0.4] - 2017-XX-XX

### Added
- Major icon updates
- Enhanced visual consistency

## Initial Releases

### [2.0] - Initial GitHub Release

### Added
- Complete UI overhaul for FFXI
- 500+ custom status icons
- Support for both 4:3 and 16:9 aspect ratios
- Updated fonts for improved readability
- Enhanced GUI skins
- Menu skins for modern displays
- Utilities included:
  - ChangeTex - Texture modification tool
  - FFXI Icon Change - Icon management utility
  - gc3_Graphics - Graphics editor
- Original ROM file backups
- Installation instructions
- Video tutorial (XI View How To.mp4)

### Changed
- Modernized FFXI interface design
- Improved status icon visibility and clarity
- Enhanced user experience for widescreen displays

## Project History

**XI View 2.0** is the continued work on the project to update FFXI's GUI to look cleaner and for status icons to be easier to understand at a glance.

**Formerly known as:**
- Brandson's UI
- FFXI Style
- XI View (from Darkshade)

### Credits & Acknowledgments

- **Darkshade**: Original XI View creator and year-long development
- **Kactuar**: Fixed Icon changer program for 32x32 icons
- **Deathbringer**: Enabled in-game font and cursor changes
- **Shinobi & Chef James**: Custom icon creation and assistance
- **Kenshi**: Contributed Master UI inclusion
- **Wildman**: Assistance and file contributions
- **All previous contributors**: For their work on earlier versions

## Version Compatibility

See [VERSION.md](VERSION.md) for detailed FFXI version compatibility matrix.

### FFXI Compatibility Overview

| XI-View Version | FFXI Version | Status |
|----------------|--------------|--------|
| June 2025 | 2.0 (June 2025) | ⚠️ Known Issue (Limbus icons) |
| April 2025 | April 2025 | ✅ Fully Compatible |
| June 2024 | June 2024 | ⚠️ Limited Support |
| Earlier | 2023 and older | ❌ Deprecated |

## Update Pattern

XI-View is updated approximately **1-3 times per year**, typically following major FFXI game updates that introduce new status effects, icons, or UI changes.

### When Updates Are Released

- After major FFXI patches
- When new status effects are added
- When existing icons break due to game updates
- When community reports compatibility issues

## Security

See [SECURITY.md](SECURITY.md) for security-related changes and vulnerability disclosure policy.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to contribute to XI-View.

## Breaking Changes

### June 2025 Update
- **Breaking**: Limbus buff icons display as "DEBUG" (Issue #41)
- **Impact**: Affects all Limbus content
- **Workaround**: Use April 2025 version or wait for fix

## Deprecated Features

None currently. All features from v2.0 onward remain supported.

## Removed Features

None. Backward compatibility maintained where possible.

## Development Notes

### Recent Improvements (2026-01-16)

This fork introduces several infrastructure improvements to support better community engagement and security:

- **Legal Clarity**: MIT License added
- **Security**: Checksums for file verification, security disclosure policy
- **Documentation**: Comprehensive contribution guidelines, version tracking
- **Transparency**: Public backlog and progress tracking

### Future Plans

See [BACKLOG.md](docs/BACKLOG.md) for planned improvements:
- Code signing for executables (P0-004)
- Comprehensive icon index (P1-001)
- Automated installation tools (P1-012)
- Cross-platform utility rewrites (P3-001)
- And more...

## Links

- **Repository**: https://github.com/thegoodguys80/XI-View
- **Original Project**: https://github.com/Caradog/XI-View
- **Issues**: https://github.com/thegoodguys80/XI-View/issues
- **License**: [MIT License](LICENSE)

## Versioning Strategy

Going forward, this project will adopt semantic versioning:

- **Major (X.0.0)**: Breaking changes or major reworks
- **Minor (2.X.0)**: New features, FFXI version updates
- **Patch (2.0.X)**: Bug fixes, minor improvements

Current version: **2.0** (transitioning to semantic versioning)

---

**Note**: This CHANGELOG was created on 2026-01-16 to improve project transparency. Earlier entries are reconstructed from commit history and may not include all details from original releases.

For the most accurate historical information, see the [git commit history](https://github.com/thegoodguys80/XI-View/commits/master).

---

**Maintained By**: thegoodguys80  
**Last Updated**: January 16, 2026  
**Format**: Based on [Keep a Changelog](https://keepachangelog.com/)