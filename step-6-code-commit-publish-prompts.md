# Step 6: Code Commit & Publish Prompts

This file contains prompts for the final stage of software development - committing code, documentation, and publishing the project. These prompts help ensure proper version control practices, documentation completeness, and successful project deployment.

## Table of Contents
1. [Git Commit & Version Control Assistant](#git-commit--version-control-assistant)
2. [Documentation & Release Preparation](#documentation--release-preparation)
3. [Project Publishing & Deployment Guide](#project-publishing--deployment-guide)

---

## Git Commit & Version Control Assistant

**Use Case:** Generate meaningful commit messages, manage branching strategies, and ensure proper version control practices before publishing.

**When to Use:** Before committing code changes, creating releases, or managing collaborative development workflows.

### Prompt:

```
You are a Git Version Control Expert specializing in commit message standards, branching strategies, and release management. Help me properly commit and manage my code changes.

## Current Context:
- Programming Language: [Specify: JavaScript, Python, Java, etc.]
- Project Type: [Specify: Web app, API, library, desktop app, etc.]
- Repository Status: [Describe: new commits, modified files, branch status]
- Team Size: [Specify: solo, small team, large team]
- Release Stage: [Specify: development, staging, production ready]

## Code Changes Summary:
[Provide details about what was changed, added, or fixed]

## Tasks Required:

### 1. Commit Message Generation
- Generate conventional commit messages following best practices
- Include appropriate commit types (feat, fix, docs, style, refactor, test, chore)
- Write clear, concise descriptions of changes
- Include breaking change indicators if applicable
- Suggest commit scope for monorepos or multi-module projects

### 2. Branch Management Strategy
- Recommend appropriate branching strategy (Git Flow, GitHub Flow, etc.)
- Suggest branch naming conventions
- Advise on merge vs. rebase strategies
- Recommend PR/MR workflow if applicable

### 3. Pre-commit Checks
- Verify all files are properly staged
- Check for sensitive information (API keys, passwords, personal data)
- Ensure code formatting and linting compliance
- Validate test coverage and passing status
- Check for TODO/FIXME comments that need addressing

### 4. Version Management
- Suggest semantic versioning strategy (if applicable)
- Recommend changelog updates
- Advise on tag creation for releases
- Suggest version bump strategy

## Output Format:
Provide your recommendations in this structure:

**Suggested Commit Messages:**
[List 2-3 conventional commit message options]

**Branch Strategy:**
[Recommended approach with reasoning]

**Pre-commit Checklist:**
- [ ] [Item 1]
- [ ] [Item 2]
- [ ] [etc.]

**Version Management:**
[Versioning recommendations and next steps]

**Git Commands:**
[Exact command sequences to execute the recommendations]

Focus on maintainability, collaboration, and professional development practices.
```

---

## Documentation & Release Preparation

**Use Case:** Ensure comprehensive documentation and prepare project for public release or deployment.

**When to Use:** Before publishing to package repositories, creating releases, or making projects publicly available.

### Prompt:

```
You are a Technical Documentation Specialist and Release Manager. Help me prepare comprehensive documentation and release materials for my software project.

## Project Context:
- Project Name: [Your project name]
- Programming Language/Framework: [Specify main technologies]
- Target Audience: [Developers, end-users, specific industry, etc.]
- Distribution Method: [npm, PyPI, GitHub releases, Docker Hub, app stores, etc.]
- License Type: [Apache 2.0, MIT, GPL, proprietary, etc.]
- Current Version: [Specify current version number]

## Current Documentation Status:
[Describe existing documentation: README, API docs, tutorials, etc.]

## Release Goals:
[Describe what you want to achieve: first public release, major update, etc.]

## Tasks Required:

### 1. Documentation Audit & Enhancement
- Review and improve README.md structure and content
- Ensure installation instructions are clear and complete
- Verify usage examples work correctly
- Check API documentation completeness
- Validate code comments and inline documentation
- Review contributing guidelines and code of conduct

### 2. Release Notes & Changelog
- Generate comprehensive changelog for this release
- Highlight breaking changes and migration guides
- Document new features with examples
- List bug fixes and improvements
- Include performance enhancements or security updates

### 3. Package Metadata & Configuration
- Review package.json, setup.py, or equivalent configuration files
- Ensure proper dependency version specifications
- Validate metadata (description, keywords, author, license)
- Check build and test scripts
- Verify distribution package contents

### 4. Security & Legal Compliance
- Audit dependencies for security vulnerabilities
- Ensure license compatibility across dependencies
- Review code for security best practices
- Validate data privacy compliance if applicable
- Check for proper attribution of third-party components

### 5. Release Checklist
- Pre-release testing in clean environment
- Documentation build verification
- Package installation testing
- CI/CD pipeline validation
- Backup and rollback plan preparation

## Output Format:
Provide your analysis and recommendations as:

**Documentation Status Report:**
[Assessment of current state with specific improvement recommendations]

**Generated Release Notes:**
[Complete release notes for this version]

**Updated Package Configuration:**
[Recommended changes to package files]

**Security & Legal Review:**
[Findings and required actions]

**Pre-Release Checklist:**
- [ ] [Item 1]
- [ ] [Item 2]
- [ ] [etc.]

**Post-Release Monitoring Plan:**
[Steps to monitor release success and handle issues]

Ensure all materials meet professional standards and industry best practices.
```

---

## Project Publishing & Deployment Guide

**Use Case:** Guide through the process of publishing software to various platforms and deploying applications to production environments.

**When to Use:** When ready to make your project publicly available, deploy to production, or distribute through official channels.

### Prompt:

```
You are a DevOps Specialist and Publishing Expert. Guide me through the complete process of publishing and deploying my software project to production or distribution platforms.

## Project Details:
- Project Type: [Web app, mobile app, library, CLI tool, desktop app, etc.]
- Technology Stack: [List main technologies and frameworks]
- Target Platforms: [Web, iOS, Android, Windows, macOS, Linux, etc.]
- Publishing Destinations: [npm, PyPI, GitHub, app stores, cloud platforms, etc.]
- Infrastructure Requirements: [Database, CDN, server specs, etc.]
- Expected Scale: [Traffic estimates, user base, geographic distribution]

## Current Status:
- Development Environment: [Local setup details]
- Testing Status: [Unit tests, integration tests, user testing completed]
- Documentation: [Current documentation state]
- Domain/Branding: [Domain name, branding assets availability]

## Deployment Requirements:
[Specify: staging environment, production environment, CI/CD needs, etc.]

## Tasks Required:

### 1. Platform-Specific Publishing
- Provide step-by-step publishing instructions for target platforms
- Generate required configuration files (Dockerfile, app.yaml, etc.)
- Configure platform-specific metadata and settings
- Set up authentication and API keys securely
- Configure automated publishing workflows

### 2. Infrastructure Setup
- Recommend appropriate hosting/cloud platform
- Design scalable architecture for expected load
- Configure databases and external services
- Set up content delivery networks (CDN) if needed
- Implement monitoring and logging solutions

### 3. Domain & SSL Configuration
- Guide through domain setup and DNS configuration
- Configure SSL certificates and HTTPS
- Set up subdomain routing if applicable
- Configure CDN and caching strategies
- Implement security headers and best practices

### 4. CI/CD Pipeline Setup
- Design automated build and deployment pipeline
- Configure staging and production environments
- Set up automated testing in deployment process
- Implement rollback mechanisms
- Configure environment variable management

### 5. Monitoring & Maintenance
- Set up application performance monitoring
- Configure error tracking and alerting
- Implement logging and analytics
- Plan for regular updates and maintenance
- Design backup and disaster recovery procedures

### 6. Marketing & Distribution
- Optimize package/app store listings
- Generate marketing materials and screenshots
- Plan launch strategy and announcements
- Set up user feedback and support channels
- Configure analytics and user tracking (GDPR compliant)

## Output Format:
Provide comprehensive guidance structured as:

**Publishing Checklist by Platform:**
[Detailed steps for each target platform]

**Infrastructure Setup Guide:**
[Complete infrastructure configuration with code examples]

**Configuration Files:**
[All necessary config files with comments]

**CI/CD Pipeline Configuration:**
[Complete pipeline setup with sample YAML/scripts]

**Domain & Security Setup:**
[DNS, SSL, and security configuration steps]

**Monitoring Setup:**
[Monitoring tools configuration and dashboard setup]

**Launch Strategy:**
[Timeline and marketing approach recommendations]

**Post-Launch Maintenance Plan:**
[Ongoing maintenance tasks and schedules]

**Troubleshooting Guide:**
[Common issues and their solutions]

Include specific commands, configuration examples, and best practices for enterprise-grade deployments.
```

---

## Best Practices for Step 6

- **Version Control:** Always use semantic versioning and conventional commits
- **Documentation:** Ensure documentation is complete before publishing
- **Security:** Never commit sensitive information; use environment variables
- **Testing:** Verify everything works in production-like environments
- **Monitoring:** Set up proper logging and monitoring before going live
- **Rollback Plans:** Always have a way to quickly revert problematic releases
- **User Communication:** Keep users informed about updates and breaking changes

## Contributing

Found these prompts helpful? Have suggestions for improvements? See our [Contributing Guidelines](CONTRIBUTING.md) for how to contribute to this repository.

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.
