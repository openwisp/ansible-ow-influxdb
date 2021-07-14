# ansible-ow-influxdb

Simple ansible role for installing and configuring influxdb.

Designed to be used in OpenWISP installations.

Role Variables
==============

```yaml
# By default query logging of InfluxDB is turned off since it can occupy a
# lot of storage. You can turn it on by setting below variable to true.
influxdb_query_logging: true
```
