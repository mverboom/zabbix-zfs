## Installation

Copy the zfs.conf file to the directory of the zabbix agent

`cp zabbix-zfs.conf /etc/zabbix/zabbix_agent2.d`

Restart the agent

`systemctl restart zabbix-agent2.service`

Import the tempate into zabbix

`zabbix-zfs.xml`

Assign the template to the systems that need to be monitored.

## Configuration

Macro's available to use for configuration:

`{$ZFSSNAPSHOTAGE}`

Defines the age after which a trigger should go of warning for an old snapshot.
The default value from the template is 1 week.

`{$ZFSSNAPSHOTEXCLUDE}`

Defines a regular expression. All snapshots matching the regex will be excluded from
triggers going off.
The default value from the template is `test`.

`{$ZFSSNAPSHOTPOOLEXCLUDE}`

Defines a comma seperated list of pool names which will not be inventoried for snapshots.
