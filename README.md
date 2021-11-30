# ansible-ow-influxdb

Simple ansible role for installing and configuring influxdb.

Designed to be used in OpenWISP installations.

Role Variables
==============

```yaml
# By default query logging of InfluxDB is turned off since it can occupy a
# lot of storage. You can turn it on by setting below variable to true.
influxdb_query_logging: true
# The username of the influxdb user that will be created.
influxdb_user_username: admin
# The password of the influxdb user that will be created.
influxdb_user_password: "your-strong-password"
# The hostname or IP address on which InfluxDB server is listening.
influxdb_http_ip: "localhost"
# The port on which InfluxDB server is listening.
influxdb_http_port: 8086
```
