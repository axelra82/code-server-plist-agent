# Autostart Code-Server

Autostart your [code-server](https://github.com/cdr/code-server) from [coder](https://coder.com) using launchd in macos.

## Instructions

The script file `code-server-agent.sh` can be placed anywhere, a good place is the user home folder, i.e. `cd ~`.

For the agent:

- place `local.code-server.plist` in `/Users/[USER_NAME]/Library/LaunchAgents/` and:
  - get your path `echo $path` and change **[YOUR_PATH]**
  - set correct path to script file in **[PATH_TO_SCRIPT]**
  - set correct user for agent **[AGENT_USER]**
- run `launchctl load /Users/[USER_NAME]/Library/LaunchAgents/local.code-server.plist` to load it (i.e. making it run in background when user logs in)

### Useful commands for debugging

Show all current services running, containing `code-server` in name
`launchctl list | grep code-server`
