echo "UserParameter=zfs.ds.master[*],/usr/local/bin/zabbix-zfs" > /etc/zabbix/zabbix_agentd.d/zfs.conf
systemctl restart zabbix-agent.service

import temlate

apply template
