# Autostart Code-Server

Autostart your [code-server](https://github.com/cdr/code-server) from [coder](https://coder.com) using launchd in macos.

## Instructions

The script file `code-server-agent.sh` can be placed anywhere, a good place is the user home folder, i.e. `cd ~`.

For the agent:

- get your path `echo $path` and change **[YOUR_PATH]**
- set correct path to script file in **[PATH_TO_SCRIPT]**
- set correct user that the agent will be running **[AGENT_USER]**
