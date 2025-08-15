# 🗓️ Day 9 / 100

100 Days of DevOps 🚀

Today's task was a bit deeper. It was to troubleshoot a mariadb server. The server was down. I tried to just start the service, but it didn't start. So, I checked the logs at `/var/log/mariadb/mariadb.log` and found an error 'Permission denied'. I first checked the file permissions and they were okay. Then I edited the service file, adding `RuntimeDirectory=mariadb` to the [Service] section, reloaded the systemd service manager, and started the mariadb service again. And it started.

![alt text](<day-9 2025-08-13 150749.png>) 
![alt text](<day-9 2025-08-13 145644.png>)