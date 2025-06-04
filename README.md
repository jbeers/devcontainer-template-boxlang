# BoxLang Dev Container Template

This repository contains a development container template for [BoxLang](https://www.boxlang.io/), a modern dynamic JVM language.

## What is BoxLang?

BoxLang is a modern dynamic JVM language that combines the best of CFML (ColdFusion Markup Language) with modern language features. It runs on the JVM and provides powerful features for web development, APIs, and enterprise applications.

## Features

This devcontainer template provides:

- **Java 21 LTS Runtime** - BoxLang runs on the JVM
- **CommandBox CLI** - The de facto standard for BoxLang development
- **BoxLang Runtime** - Latest stable version pre-installed
- **VS Code Extensions** - BoxLang language support and tooling
- **Git Integration** - Pre-configured Git setup
- **Development Tools** - Essential utilities for BoxLang development

## Quick Start

1. **Prerequisites**: Ensure you have Docker and VS Code with the Dev Containers extension installed.

2. **Use this template**:
   - Click "Use this template" to create a new repository
   - Clone your new repository locally
   - Open in VS Code

3. **Open in Dev Container**:
   - VS Code will detect the devcontainer configuration
   - Click "Reopen in Container" when prompted
   - Or use Command Palette: `Dev Containers: Reopen in Container`

4. **Start developing**:
   ```bash
   # Create a new BoxLang project
   box create app myapp
   cd myapp
   
   # Start the development server
   box server start
   ```

## Template Structure

```
src/boxlang/
├── .devcontainer/
│   ├── devcontainer.json    # Dev container configuration
│   ├── Dockerfile          # Custom container definition
│   └── docker-compose.yml  # Multi-container setup
├── .vscode/
│   ├── extensions.json     # Recommended extensions
│   ├── settings.json       # VS Code settings
│   └── tasks.json         # Build and run tasks
├── box.json               # BoxLang project configuration
├── Application.bx         # Sample BoxLang application
├── index.bx              # Sample BoxLang file
└── README.md             # Template documentation
```

## What's Included

### Runtime Environment
- **CommandBox CLI** latest version
- **BoxLang Runtime** latest stable
- **Node.js & npm** for frontend tooling
- **Git** for version control

### VS Code Extensions
- **BoxLang Language Support** - Syntax highlighting, IntelliSense
- **TestBox TDD/BDD Support** - Testing framework integration
- **CFML Language Support** - Enhanced CFML/BoxLang features
### Development Tools
- CommandBox package manager
- BoxLang REPL
- Hot reload development server
- Debugging capabilities
- Testing framework (TestBox)

## Customization

### Modify Java Version
Edit the `Dockerfile` to change the Java version:
```dockerfile
FROM eclipse-temurin:17-jdk-jammy  # Change to desired version
```

### Add Additional Tools
Add packages to the `Dockerfile`:
```dockerfile
RUN apt-get update && apt-get install -y \
    your-additional-package \
    && rm -rf /var/lib/apt/lists/*
```

### Configure VS Code Settings
Modify `.vscode/settings.json` to customize the development environment.

## Contributing

Contributions are welcome! Please feel free to submit issues and pull requests.

## Resources

- [BoxLang Documentation](https://boxlang.ortusbooks.com/)
- [BoxLang Website](https://www.boxlang.io/)
- [CommandBox Documentation](https://commandbox.ortusbooks.com/)
- [VS Code Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers)

## License

This template is released under the MIT License. See [LICENSE](LICENSE) for details.
