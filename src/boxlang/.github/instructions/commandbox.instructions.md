# CommandBox Instructions


## Overview

CommandBox is a CLI tool for working with BoxLang and CFML projects. It has many features related to

- package management
- server management
- dependency management
- testing

CommandBox can be used to run single commands like `box server start` or you can run it interactively like a shell by simply executing `box` and then using stdin and stdout to communicate.

If you want to run CommandBox scripts in order to meet a specific goal then you should look for a terminal that is being used for CommandBox. If one doesn't exists create a terminal named `CommandBox` and use that for your commands. Instantiate Commandbox by running `box` in the terminal and resuse it for all your commands.

CommandBox has a very useful help system that you can query to find out more about the commands available. You can run `box help` to see a list of commands or `box help <command>` to see more information about a specific command.
You can also use the `box help` command to see a list of available packages and their commands.

## Example CommandBox Commands

Install a boxlang module
```bash
box install bx-mysql
```

Check the server status
```bash
box server status
```

Restart the server
```bash
box server restart
```

View the server logs
```bash
box server log
```

## Box.json

CommandBox projects can have a `box.json` file that defines the project and its dependencies. This file is similar to a `package.json` file in Node.js or a `pom.xml` file in Maven.

Query this file if you need to check what packages are installed or what commands are available in the project.