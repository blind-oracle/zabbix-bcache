# zabbix-bcache

Zabbix template & script to monitor BCache - Linux block device caching layer

## Features

- Low level discovery of BCache devices (bcacheN), Cache sets and Cache devices
- Collection of all important metrics
- Several triggers (IO errors, state etc)
- Macros to customize trigger behavior
- Single Python script to do discovery & get items
- Usage of dependent items & jsonpath - only a single call per device type to get a JSON
- Zabbix agent passive mode

## Requirements

- Tested on Zabbix 5.0, but should work on 4.2+
- Python3

## Installation

- Place `bcache.conf` in `/etc/zabbix/zabbix_agentd.d`
- Place `bcache.py` in `/etc/zabbix/scripts`
  You can put it into any other place, but then you'll have to adjust `bcache.conf`
- Restart `zabbix-agentd`
- Import `template_bcache.xml`
- You're good to go
