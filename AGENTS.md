# AGENTS.md

This file provides guidance for AI agents working with this repository.

## Project Overview

This is a simple static website for **nexus-stack.ch**, hosted via GitHub Pages.

## GitHub Repository

- **Repository**: [stefanko-ch/nexus-stack.ch](https://github.com/stefanko-ch/nexus-stack.ch)
- **Owner**: stefanko-ch
- **Default Branch**: main
- **GitHub Pages URL**: https://nexus-stack.ch

This website is directly linked to the GitHub repository. All source files are managed in this repository, and the site is automatically deployed via GitHub Pages whenever changes are pushed to the `main` branch.

## Repository Structure

```
├── CNAME                           # Custom domain configuration for GitHub Pages
├── index.html                      # Main landing page
├── README.md                       # Project documentation
├── AGENTS.md                       # AI agent instructions (this file)
├── .nexus-version                  # Latest Nexus-Stack version (auto-updated)
└── .github/
    └── workflows/
        └── update-content.yml      # Auto-update workflow triggered by Nexus-Stack releases
```

## Technology Stack

- **Type**: Static Website
- **Hosting**: GitHub Pages
- **Domain**: nexus-stack.ch

## Automated Content Updates

This website automatically syncs content from the main [Nexus-Stack](https://github.com/stefanko-ch/Nexus-Stack) repository:

1. When a new release is created in Nexus-Stack, it triggers a `repository_dispatch` event
2. The `update-content.yml` workflow in this repo receives the event
3. The workflow fetches the latest README.md and extracts relevant content
4. Changes are automatically committed and deployed via GitHub Pages

### Required Secret

The Nexus-Stack repo needs a `WEBSITE_DISPATCH_TOKEN` secret (Personal Access Token with `repo` scope) to trigger the update workflow.

## Development Guidelines

### HTML/CSS
- Keep the code clean and semantic
- Use modern HTML5 standards
- Ensure responsive design for mobile devices
- Optimize for performance and accessibility

### File Structure
- Keep the structure flat and simple
- All static assets should be in the root or organized in dedicated folders (e.g., `/assets`, `/css`, `/js`)

### Deployment
- Changes pushed to the `main` branch are automatically deployed via GitHub Pages
- The `CNAME` file maintains the custom domain configuration - do not modify unless intentionally changing the domain

## Code Style

- Use consistent indentation (2 or 4 spaces)
- Add meaningful comments where necessary
- Keep files organized and well-structured

## Testing

- Test changes locally before pushing
- Verify the site renders correctly on different browsers and devices
- Check that all links and resources load properly

## Disclaimer

This is an **independent open-source project** released under the **MIT License** with no commercial intentions. "Nexus Stack" is not affiliated with, endorsed by, or connected to any other companies or products using similar names, including but not limited to:

- **Sonatype Nexus Repository** - Artifact repository manager by Sonatype Inc.
- **Nexus Mods** - Gaming modification platform
- **Google Nexus** - Former Google smartphone line
- **Nexus (Blockchain)** - Blockchain platform by Nexus.io
- Any other trademark holders using "Nexus" in their branding

All other trademarks are the property of their respective owners.

## Contact

For questions about this project, please reach out to the repository owner.
