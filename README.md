# Autostart Code-Server

Autostart your [code-server](https://github.com/cdr/code-server) from [coder](https://coder.com) using launchd in macos.

## Instructions

### Script

The script file `code-server-agent.sh` can be placed anywhere, a good place is the user home folder, i.e. `cd ~`.

Change **[*VPS_NAME]** to what you want your server name to be, this will result in the virtual private server name and your github username, i.e. `https://your_custom_vps_name-your_github_username.cdr.co/`.

**NOTE!** If you want to use the default VPS name when code-server starts, simply remove **[*VPS_NAME]**.

### Agent

- place `local.code-server.plist` in `/Users/[USER_NAME]/Library/LaunchAgents/` and:
  - get your path `echo $path` and change **[YOUR_PATH]**
  - set correct path to script file in **[PATH_TO_SCRIPT]**
  - set correct user for agent **[AGENT_USER]**
- run `launchctl load /Users/[USER_NAME]/Library/LaunchAgents/local.code-server.plist` to load it (i.e. making it run in background when user logs in)

### Useful commands for debugging

Show all current services running, containing `code-server` in name
`launchctl list | grep code-server`
