EVM - Simple Elasticsearch Version Manager
==========================================

**EVM** is a simple bash script used for development to manage different versions of Elasticsearch on your local machine.

## Installation
```sh
wget https://raw.githubusercontent.com/duydo/evm/master/evm -O '/usr/local/bin/evm'
```

## Usage
```sh
evm  -h                                   Print help information
evm  -V                                   Print version information
evm  list                                 List all installed Elasticsearch versions
evm  version                              Print the current activated Elasticsearch version
evm  install <version>                    Install a specific Elasticsearch version
evm  use <version>                        Use a specific Elasticsearch version
evm  remove <version>                     Remove a specific Elasticsearch version if available
evm  which [<version>]                    Print path to installed Elasticsearch version
evm  plugin list                          List all installed Elasticsearch plugins
evm  plugin <install|remove> <plugin>     Install or remove an Elasticsearch plugin
evm  start [-c </path/to/config/dir>]     Start Elasticsearch with/without a specific config directory
```
## Example
```sh
evm  install 5.3.1                        Install Elasticsearch 5.3.1
evm  use 5.3.1                            Use Elasticsearch 5.3.1
evm  start                                Start Elasticsearch node with the default config directory
evm  start -c /etc/elasticsearch          Start Elasticsearch node with /etc/elasticsearch config directory
evm  plugin install x-pack                Install the x-pack plugin
evm  plugin remove x-pack                 Remove the x-pack plugin
```
## Note
To uninstall, just remove the $EVM_HOME folder (usually ~/.evm)

## Licence
    This software is licensed under the Apache License, version 2 ("ALv2"), quoted below.

    Copyright 2017 Duy Do

    Licensed under the Apache License, Version 2.0 (the "License"); you may not
    use this file except in compliance with the License. You may obtain a copy of
    the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
    WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
    License for the specific language governing permissions and limitations under
    the License.
