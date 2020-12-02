# zabbix-bcache

Zabbix template to monitor BCache - Linux block device caching layer

## Features

- Low level discovery of BCache devices (bcacheN), Cache sets and Cache devices
- Collection of all important metrics
- Several triggers
- Single Python script to do discovery & get items
- Usage of dependent items & jsonpath - only a single call per device type to get a JSON
- Zabbix agent passive mode

## Requirements

- Tested on Zabbix 5.0, but should work on 4.2+
- Python3

## Installation

- Put `bcache.conf` info `/etc/zabbix/zabbix_agentd.d` directory
- Put `bcache.py` into `/etc/zabbix/scripts` directory.
  Or in any other, but you'll have to edit `bcache.conf` then
- Restart `zabbix-agentd`
- Import `template_bcache.xml`
- You're good to go
