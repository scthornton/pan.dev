# Security Policy

## Developer Documentation Platform

This repository contains the **pan.dev documentation platform**, a Docusaurus 2-based developer documentation site for Palo Alto Networks. This is a **community-supported open-source project** providing comprehensive developer resources and API documentation.

### Platform Purpose

**pan.dev** provides:
- ✅ Developer-focused documentation for Palo Alto Networks products
- ✅ OpenAPI specifications and API references
- ✅ Integration guides and code examples
- ✅ SDK documentation and tutorials
- ✅ Community-contributed content improvements

**Important:** This is a **documentation platform**. Security issues with Palo Alto Networks products should be reported through official security channels (see below).

## Reporting Security Issues

### Documentation Platform Security

**For security issues with the pan.dev documentation site itself** (not products):

**Email:** scott@perfecxion.ai

Report issues such as:
- XSS vulnerabilities in the documentation platform
- Malicious code in site infrastructure
- Security issues with the Docusaurus setup
- Vulnerable dependencies in package.json
- Build or deployment pipeline security concerns

**Response Timeline:**
- **Initial Response**: Within 48 hours
- **Assessment**: Within 7 days
- **Resolution**: Based on severity

### Product Security Issues

**For security vulnerabilities in Palo Alto Networks products** (not the documentation site):

**Palo Alto Networks Security Advisory**:
- Visit: https://security.paloaltonetworks.com/
- Email: psirt@paloaltonetworks.com

**Scope**: All security issues related to:
- Network security products and services
- Cloud-delivered security services
- APIs and SDKs (product functionality, not docs)
- Product vulnerabilities or exploits

**Separation of Concerns**:
- **Documentation site security** → scott@perfecxion.ai (this repository)
- **Product security** → psirt@paloaltonetworks.com (official PSIRT)

## Documentation Site Security

### Static Site Security

**Architecture**:
- Docusaurus 2 static site generator (React-based)
- All content pre-generated as HTML/CSS/JavaScript
- No server-side code execution
- No database or user data storage
- Firebase hosting with HTTPS encryption

**Security Features**:
- Static content delivery (no dynamic execution)
- HTTPS enabled for all connections
- GitHub Actions security scanning (CodeQL)
- Dependency vulnerability monitoring
- No user authentication or session management

### Content Security

**Documentation Guidelines**:
- All code examples reviewed before publication
- No credentials, API keys, or secrets in examples
- Sanitized logs and configurations
- Placeholder values for sensitive data
- Security warnings in appropriate sections

**OpenAPI Security**:
- API specifications reviewed for sensitive data exposure
- No real credentials in API examples
- Authentication guidance clearly documented
- Security best practices included in API docs

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| master  | :white_check_mark: |

**Note**: The master branch is the live production branch for pan.dev and receives continuous updates.

## Security Best Practices

### For Contributors

**1. Content Security**
- Review all code examples for security issues
- Remove any credentials or API keys before committing
- Use placeholder values (e.g., `YOUR_API_KEY`)
- Include security warnings for risky operations
- Test code examples in isolated environments

**2. Dependency Management**
- Keep Docusaurus and plugins updated
- Review dependency security advisories
- Run `yarn audit` regularly
- Update vulnerable dependencies promptly
- Follow semantic versioning for updates

**3. Code Quality**
- Use Prettier for consistent formatting
- Follow TypeScript best practices
- Enable ESLint security rules
- Run pre-commit hooks (Husky)
- Validate builds before committing

**4. API Documentation**
- Never include real API credentials
- Document authentication requirements clearly
- Provide security best practices for each API
- Highlight rate limiting and access control
- Include error handling guidance

### For Documentation Users

**1. Code Example Usage**
- Verify examples before implementing in production
- Replace placeholder values with real credentials securely
- Follow security best practices for your environment
- Don't hardcode credentials in source code
- Use environment variables or secrets management

**2. API Security**
- Follow authentication guidelines carefully
- Implement proper access control
- Use TLS/SSL for all API communications
- Rotate API keys regularly
- Monitor API usage for anomalies

**3. Responsible Disclosure**
- If you discover vulnerabilities in products, contact psirt@paloaltonetworks.com
- Follow responsible disclosure timelines (90 days)
- Don't publicly disclose before vendor coordination
- Provide clear reproduction steps

## Dependency Security

### Automated Scanning

**GitHub Actions**:
- CodeQL analysis on all commits
- Dependency vulnerability scanning
- Automated security updates via Dependabot

**Manual Reviews**:
- Quarterly dependency audit (`yarn audit`)
- Review of critical security advisories
- Evaluation of dependency alternatives
- Update strategy for breaking changes

### Known Dependencies

**Core Dependencies**:
- Docusaurus 2 (documentation framework)
- React (UI library)
- TypeScript (type safety)
- Prettier (code formatting)
- Playwright (end-to-end testing)

**Security Considerations**:
- All dependencies pinned in package.json
- Lock file (yarn.lock) committed to repository
- Regular updates via GitHub Actions and Dependabot
- Security advisories monitored continuously

## Build and Deployment Security

### GitHub Actions

**Workflows**:
- `deploy-live.yml`: Production deployment to Firebase
- `codeql-analysis.yml`: Security scanning with CodeQL

**Security Measures**:
- Secrets stored in GitHub Actions secrets
- Limited workflow permissions (principle of least privilege)
- Branch protection rules on master
- Required reviews for pull requests
- Automated security checks before merge

### Firebase Deployment

**Security**:
- HTTPS enforced for all connections
- Firebase security rules configured
- Access logs enabled for monitoring
- Automated deployment from master only
- Preview deployments isolated per PR

## Community Support Model

### Support Policy

As documented in [SUPPORT.md](SUPPORT.md), this project follows Palo Alto Networks' **community-supported policy**:

- Best-effort support from community and Palo Alto Networks experts
- No SLA or guaranteed response times
- Product support through official channels only
- Documentation improvements welcomed via pull requests
- Security issues prioritized for rapid response

### Contribution Security

**Pull Request Review**:
- All PRs require review before merge
- Security-focused code review for sensitive changes
- Automated checks (linting, testing, security scanning)
- Preview deployments for validation
- Community feedback period for major changes

## Privacy

### No Personal Data Collection

**Documentation Site**:
- No user accounts or authentication
- No cookies or local storage of personal data
- No tracking scripts or analytics by default
- Public content only (no private data)

**Third-Party Services**:
- Firebase hosting (aggregate statistics only)
- GitHub (standard repository access logs)
- Google Tag Manager (if configured, respects DNT)

## Compliance

### Open Source Licensing

**Repository License**: See [LICENSE](LICENSE)
- Open source project with community contributions
- Attribution required per license terms
- Derivative works subject to license restrictions

### Content Attribution

**Documentation Standards**:
- Proper attribution for third-party content
- Respect for intellectual property
- Fair use of referenced materials
- Linking to original sources

## Contact

### Security Concerns

**Documentation Site Issues**: scott@perfecxion.ai
**Product Security Issues**: psirt@paloaltonetworks.com

### General Contact

- **Email:** scott@perfecxion.ai
- **Alternative:** scthornton@gmail.com
- **GitHub:** [@scthornton](https://github.com/scthornton)

For questions about this documentation platform repository (not product security), contact scott@perfecxion.ai.

### Official Palo Alto Networks Resources

- **Security Advisories**: https://security.paloaltonetworks.com/
- **PSIRT Email**: psirt@paloaltonetworks.com
- **Support Portal**: https://support.paloaltonetworks.com/
- **Developer Resources**: https://pan.dev/

---

**Note**: This SECURITY.md covers the pan.dev documentation platform repository. For security issues with Palo Alto Networks products, use official security reporting channels (psirt@paloaltonetworks.com).
