# Changelog

## 0.2.0 (2026-08-03)

* Fix install/upgrade removing the whole `$HOME/.local/lib` folder instead of only `$HOME/.local/lib/rakpios-cli`
* Stop overwriting the user's `~/.tmux.conf`; the log viewer now uses its own config file in `$HOME/.config/rakpios-cli`
* Fix network configuration not finding the existing connection of an interface, creating a second competing profile instead of reconfiguring it
* Fix services with an environment variable containing spaces not being deployable, such as the default `TC_KEY` of LoRa Basics Station
* Fix the update check never announcing a new version, as versions were compared as plain text, and comparing the local tag against the latest release instead of the latest tag
* Fix the installation quitting silently when a dependency was missing and the tool was installed with the piped command from the README
* Fix the Gateway EUI not being shown after deploying LoRa Basics Station, whose title no longer matched the one the tool looked for; the EUI is now read from the container itself
* Fix start, stop, remove and logs acting on the wrong kind of service when reached from the deploy menu
* Fix DHCP configuration silently doing nothing when the interface had no connection yet
* Fix switching a WiFi connection from secured to open leaving the previous security settings behind
* Fix an empty passphrase aborting the WiFi setup instead of configuring an open network, as the prompt offers
* Fix the WiFi scan list keeping the entries of the previous scan, and trailing blanks in the selected SSID
* Fix removing an existing access point, which never matched the connection to delete
* Fix services without environment variables showing an error on top of the menu
* Fix the environment variables not being listed alphabetically
* Fix the service log window showing the whole history instead of the last minutes
* Fix a service name being confused with another one that contains it
* Fix the Docker check, which could not detect a permission problem
* Fix the service log window reattaching to a previous log session instead of showing the selected service
* Fix `git` not being checked as a dependency, although the installation uses it
* Deploying a compose service no longer leaves the tool inside the stack folder
* Post-up notes no longer show an empty host address when no interface can be determined
* Build the docker commands as argument lists instead of evaluating strings
* Replace the menu recursion with loops
* Add a shellcheck workflow

## 0.1.5 (2025-11-07)

* Show the status of the current service in the title
* Bring up the compose file from its own folder
* Simplify the service menu

## 0.1.4 (2024-10-14)

* Fix installation issue in libraries

## 0.1.3 (2024-10-07)

* Fix installation issue when $HOME/.local/lib not existing

## 0.1.2 (2024-03-14)

* Code maintenance and clean up
* Sort environment variables alphabetically
* Rename menus to make them more intelligible
* Improve WiFi AP set up

## 0.1.1 (2024-03-04)

* Fix getting `gateway_eui` from UDP and BasicStation latest images
* Fix rakpios-cli version retrieval

## 0.1.0 (2023-12-28)

* Add a time delay to fix the post-up info error for the UDP packet forwarder service
* Remove the portainer specific code from rakpios-cli by @kkcloudy in https://github.com/RAKWireless/rakpios-cli/pull/2
* Update rakpios-cli-service-deploy by @kkcloudy in https://github.com/RAKWireless/rakpios-cli/pull/3
* Add service log feature by @Sheng2216 in https://github.com/RAKWireless/rakpios-cli/pull/4
* Add a time delay to fix the post-up info error for the UDP packet forwarder service by @Sheng2216 in https://github.com/RAKWireless/rakpios-cli/pull/5
