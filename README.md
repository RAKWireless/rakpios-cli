# RAKPiOS-cli

The rakpios-cli is a command line tool tailored for RAKPiOS. Users can use rakpios-cli to manage network connections and deploy various IoT services from a curated list of docker containers.

## Quick Start Guide

Users can use remote bash execution script to install/upgrade rakpios-cli.

To install:

`curl https://raw.githubusercontent.com/RAKWireless/rakpios-cli/main/rakpios-cli -sSf | bash -s -- --install --silent && source ~/.profile`

To update:

`curl https://raw.githubusercontent.com/RAKWireless/rakpios-cli/main/rakpios-cli -sSf | bash -s -- --upgrade --silent && source ~/.profile`

After the installation/upgrade is finished, users can use the command `rakpios-cli` to launch this tool. To display help infomation, please add the flag `--help` or `-h`

```
rak@rakpios:~ $ rakpios-cli --help
rakpios-cli
The command line tool for RAKPiOS
USAGE:
    rakpios-cli [FLAGS]
FLAGS:
    -d, --debug             Prints debug message
    -h, --help              Prints help information
    -i, --install           Install rakpios-cli
    -u, --upgrade           Upgrade rakpios-cli
    -s, --silent            Perform install/update silently (no user interaction)
    -v, --version           Prints version information
```

There are three options list in the main menu: Manage networks, Deploy services, and List services. You will need specific privileges to make changes to your network connections, and you need to make sure the current user has access to **docker**.
