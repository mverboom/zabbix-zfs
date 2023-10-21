## Installation

Copy the zfs.conf file to the directory of the zabbix agent

`cp zabbix-zfs.conf /etc/zabbix/zabbix_agent2.d`

Restart the agent

`systemctl restart zabbix-agent2.service`

Import the tempate into zabbix

`zabbix-zfs.xml`

Assign the template to the systems that need to be monitored.
