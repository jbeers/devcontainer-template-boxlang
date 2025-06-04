# CommandBox Dev Container Template

A development container template for BoxLang and CFML development using [CommandBox](https://commandbox.ortusbooks.com/) and multiple engine support.

## Features

- **Multi-Engine Support**: Choose from BoxLang, Lucee 5/6, or Adobe ColdFusion 2021/2023
- **CommandBox CLI**: Pre-installed with package management and server capabilities
- **VS Code Integration**: BoxLang & CFML language support, syntax highlighting, and debugging
- **Development Tools**: Git, Node.js LTS, and common utilities

## Quick Start

1. Install [VS Code](https://code.visualstudio.com/) with the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
2. Create a new repository from this template or add to existing project
3. Open in VS Code and select "Reopen in Container" when prompted
4. Choose your preferred CFML engine during setup

## Engine Options

- **boxlang** - Latest BoxLang stable release
- **boxlang-snapshot** - BoxLang development snapshot  
- **lucee5** - Lucee 5.x
- **lucee6** - Lucee 6.x
- **adobe2021** - Adobe ColdFusion 2021
- **adobe2023** - Adobe ColdFusion 2023

## What's Included

### Container Environment
- CommandBox CLI with selected CFML engine
- Git and GitHub CLI
- Node.js LTS for frontend tooling
- Common development utilities (curl, vim, nano)

### VS Code Extensions
- CFML language support and syntax highlighting
- CommandBox and TestBox integration
- Git integration with GitLens
- JSON and YAML support

### Development Configuration
- Port forwarding for web server (8080)
- VS Code tasks for common CommandBox operations
- File associations for CFML file types
- Workspace settings optimized for CFML development

## Project Structure

```
.devcontainer/
├── devcontainer.json    # Container configuration
├── docker-compose.yml   # Service definitions
└── Dockerfile          # Container build instructions

.vscode/
├── extensions.json      # Recommended extensions
└── settings.json       # Workspace settings
```

## Contributing

Issues and pull requests welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

MIT License - see [LICENSE](LICENSE) for details.