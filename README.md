# Zabbix-Templates
This repo contains various different zabbix templates. 

## Zabbix-DB-Partitions
This template runs an SSH check for the number of DB partitions for your environment. You may want to add more checks for additional days in the future, to do so you just need to copy the item and update the `XXXXXXXX` value for the check:

```
ls /var/lib/mysql/zabbixdb | grep -c $(date -d "$(date +%F)"+XXXXXXXXdays "+%Y%m%d")
```

***Note*** You will likely need to change the `ls /var/lib/mysql/zabbixdb` location to be where your `Zabbix` database lives on the host you are checking. 
