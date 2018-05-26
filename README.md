# We can monitor your redis in zabbix by userdefined items by userparameters #

In the redis server: 

Run a cronjob for every 2 minutes to collect redis server parameters as arguments:

 #sudo crontab -e

*/2 * * * * /usr/bin/redis-cli info > /tmp/redismetric

And add userparameter_redis.conf in the /etc/zabbix/zabbix_agent.conf.d/

# And then add the following parameters in zabbix UI:

Go to Zabbix UI > configuration > host > item > create item > key > enter the key
