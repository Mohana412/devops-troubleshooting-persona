Step 1 System health check

uptime
top
free -m
df -h

Step 2 Process investigation

ps -ef
ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%cpu | head

Step 3 Service verification

systemctl status service_name

Step 4 Log analysis

journalctl -xe
tail -100 /var/log/messages

Step 5 Network diagnostics

ping hostname
ss -tulnp
curl endpoint