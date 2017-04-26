EVM - Simple Elasticsearch Version Manager
==========================================

**EVM** is a simple bash script used for development to manage different versions of Elasticsearch on your local machine.

## Installation
```sh
wget https://raw.githubusercontent.com/duydo/evm/master/evm -O '/usr/local/bin/evm'
```

## Usage
```sh
evm list                                           List all versions of Elasticsearch have been installed
evm install <version>                              Install a specific Elasticsearch version
evm remove <version>                               Remove a specific Elasticsearch version
evm use <version>                                  Use a specific Elasticsearch version
evm plugin [<--install|--remove> <plugin>]         Install/remove Elasticsearch plugin.
evm start [--config-path </path/to/config/dir>]    Start Elasticsearch node with/without a specific config directory
evm help                                           Display usage information
```
## Example
```sh
evm install 5.3.1                                  Install Elasticsearch 5.3.1
evm use 5.3.1                                      Use Elasticsearch 5.3.1
evm start                                          Start Elasticsearch node with defaut config directory
evm start --config-path /etc/elasticsearch         Start Elasticsearch node with /etc/elasticsearch config directory
evm plugin --install x-pack                        Install the x-pack plugin
evm plugin --remove x-pack                         Remove the x-pack plugin
```
## Note
To remove, delete or uninstall evm - just remove the $EVM_HOME folder (usually ~/.evm)
