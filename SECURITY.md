# Security Policy

## Reporting a Vulnerability

We take the security of XI-View seriously. If you discover a security vulnerability, please help us protect our users by reporting it responsibly.

### How to Report

**DO NOT** create a public GitHub issue for security vulnerabilities.

Instead, please report security issues to:
- **Email**: Create an issue with the title "SECURITY: [Brief Description]" and mark it with the `security` label
- **Direct Contact**: Open a GitHub issue and request private disclosure

### What to Include

When reporting a vulnerability, please include:
- Description of the vulnerability
- Steps to reproduce the issue
- Potential impact
- Affected versions
- Any suggested fixes (if applicable)

### Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 7 days
- **Fix Timeline**: Varies by severity (see below)

## Severity Levels

### Critical (Fix within 7 days)
- Remote code execution
- Privilege escalation
- Data loss or corruption
- Malicious file injection

### High (Fix within 14 days)
- Local code execution
- Unauthorized file access
- Security bypass

### Medium (Fix within 30 days)
- Information disclosure
- Configuration vulnerabilities
- Denial of service

### Low (Fix within 90 days)
- Minor security improvements
- Hardening recommendations

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 2.0 (June 2025) | ✅ Yes |
| April 2025 | ✅ Yes (maintenance) |
| June 2024 | ⚠️ Limited |
| Older versions | ❌ No |

## Security Best Practices

### For Users

1. **Verify Downloads**
   - Always check CHECKSUMS.txt before installation
   - Download only from official sources (GitHub releases)
   - Verify the repository URL: `github.com/thegoodguys80/XI-View`

2. **Backup First**
   - Use included backups in `00 - Original Backup/`
   - Create your own backup before installation
   - Test in non-critical environment first

3. **Keep Updated**
   - Subscribe to repository notifications
   - Check for updates regularly
   - Review release notes for security fixes

4. **Antivirus Warnings**
   - Unsigned executables may trigger warnings
   - Check CHECKSUMS.txt to verify authenticity
   - See Issue #42 regarding false positives

### For Contributors

1. **Code Review**
   - All code changes require review
   - Security-sensitive changes need thorough testing
   - Document security implications

2. **Dependencies**
   - Regularly audit for vulnerabilities
   - Keep utilities updated
   - Document version requirements

3. **Testing**
   - Test on clean FFXI installation
   - Verify backup/restore functionality
   - Check for file permission issues

## Known Security Considerations

### 1. Unsigned Executables
- **Status**: Known issue (see Issue #42)
- **Risk**: False positive antivirus detections
- **Mitigation**: Code signing certificate planned (P0-004)
- **Workaround**: Verify checksums, run in sandbox

### 2. File Overwrites
- **Status**: By design
- **Risk**: Overwrites game files
- **Mitigation**: Backups included, documented process
- **Workaround**: Manual backup before installation

### 3. Binary Files
- **Status**: Inherent to project type
- **Risk**: DAT files are binary, not human-readable
- **Mitigation**: Checksums, source backups
- **Workaround**: Compare with original files

### 4. Windows-Only Tools
- **Status**: Current limitation
- **Risk**: Limited audit of closed-source utilities
- **Mitigation**: Tools from trusted community members
- **Future**: Open-source alternatives planned (P3-001)

## Security Improvements in Progress

### Completed ✅
- MIT License added for legal clarity
- SHA-256 checksums for file verification
- Version compatibility tracking

### In Progress 🔄
- Code signing certificate (P0-004)
- Automated security scanning in CI/CD (P1-007)
- GPG-signed releases (P1-008)

### Planned 📋
- Open-source utility rewrites (P3-001)
- Automated backup tool (P1-013)
- Installation validator (P1-012)

## Disclosure Policy

We follow responsible disclosure principles:

1. **Private Disclosure**: Report sent to maintainers privately
2. **Acknowledgment**: We confirm receipt within 48 hours
3. **Investigation**: We assess and verify the issue
4. **Fix Development**: We develop and test a fix
5. **Coordinated Release**: We release fix and notify reporter
6. **Public Disclosure**: We publish security advisory after fix is available

### Credit

We will acknowledge security researchers who report valid vulnerabilities (unless they prefer to remain anonymous).

## Contact

- **Repository**: https://github.com/thegoodguys80/XI-View
- **Issues**: https://github.com/thegoodguys80/XI-View/issues
- **Fork Owner**: @thegoodguys80
- **Original Project**: https://github.com/Caradog/XI-View

## Additional Resources

- [VERSION.md](VERSION.md) - Version compatibility and known issues
- [CHECKSUMS.txt](CHECKSUMS.txt) - File integrity verification
- [LICENSE](LICENSE) - Project license terms

---

**Last Updated**: January 16, 2026  
**Version**: 1.0  
**Maintained By**: thegoodguys80

*This security policy applies to the XI-View fork maintained at github.com/thegoodguys80/XI-View*