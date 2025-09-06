# 🗓️ Day 18 / 100

100 Days of DevOps 🚀

Configured app servers, and the database server to host a WordPress website.


✅ Installed httpd, PHP and the PHP MySQL Native Driver packages on the app servers.

✅ Set the port number in the httpd config file to the required port number and started the service.

✅ In the database server, installed the mariadb and mariadb-server packages and started the mariadb service.

✅ Used the mysql CLI tool to create the database, create the user, and grant all database privileges to the database user, and flush privileges. The database user created was how the app servers would access the database.

```CREATE DATABASE database_name;
    CREATE USER 'database_user'@'%' IDENTIFIED AS 'password';
    GRANT ALL PRIVILEGES ON database_name.* TO 'database_user'@'%';
    FLUSH PRIVILEGES; 
```

✅ Made sure everything was running as intended.


![Displaying the PHP webpage](<images/day-18.png>)