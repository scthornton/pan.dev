# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Comprehensive developer documentation platform for Palo Alto Networks
- Docusaurus 2-based static site generator with modern developer experience
- Aggregated developer-focused content across Palo Alto Networks products
- Open-source contribution model for community documentation improvements
- Multi-product documentation coverage with OpenAPI specifications

### Platform Features

**Documentation Site (pan.dev)**:
- **Docusaurus 2**: Modern static site generator with live reload
- **Markdown Authoring**: Easy-to-write documentation format
- **Contributing Guide**: Community contribution workflow and guidelines
- **Firebase Deployment**: Automated deployment from master branch
- **Build/Deploy Previews**: PR preview deployments for review

**Developer Tools**:
- **OpenAPI Specifications**: API documentation for Palo Alto Networks products
- **Code Examples**: Sample implementations and usage patterns
- **Interactive Docs**: API explorers and testing interfaces
- **Version Management**: Multi-version documentation support

### Content Organization

**Product Documentation**:
- Network security platform APIs
- Cloud-delivered security services
- Management and orchestration tools
- Developer SDKs and libraries
- Integration guides and tutorials

**Documentation Structure**:
- Products directory with auto-generated API docs
- Static site generation with Docusaurus config
- Custom plugins (GTM, OpenAPI integration)
- Localized content and internationalization support

### Technical Stack

**Core Technologies**:
- **Docusaurus 2**: React-based documentation framework
- **TypeScript**: Type-safe configuration and plugins
- **Yarn**: Package management and build tooling
- **Firebase**: Hosting and deployment platform
- **Playwright**: End-to-end testing framework

**Development Workflow**:
- Local development server with hot reload (`yarn start`)
- Production build generation (`yarn build`)
- Continuous integration with GitHub Actions
- Automated CodeQL security scanning
- Husky pre-commit hooks for code quality

### Community Contributions

**Open Source Model**:
- Public GitHub repository for community access
- Contribution guidelines for authors and editors
- Issue tracking for documentation improvements
- Pull request workflow with preview deployments
- Community-supported maintenance model

**Contributors**: Recognition for all community members who have contributed to improving the documentation

### Automation and CI/CD

**GitHub Actions**:
- Deploy Live workflow for production deployments
- CodeQL analysis for security scanning
- Automated build verification on pull requests
- Deploy preview generation for PR reviews

**Quality Assurance**:
- Prettier code formatting and linting
- Husky pre-commit hooks
- Playwright end-to-end testing
- GitLab CI/CD integration support

### Support Model

**Community-Supported**: As documented in SUPPORT.md, this documentation site follows Palo Alto Networks' community-supported policy with best-effort maintenance and expert contributions as available.

[Unreleased]: https://github.com/scthornton/pan.dev/commits/master
