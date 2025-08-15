# 🗓️ Day 10 / 100

100 Days of DevOps 🚀

I created a script to backup a webserver to a backup server. How I went about it:

1️⃣ Wrote the script to zip up the `/var/www/html/official` directory, copy it to the `/backup/ directory `and copy it to the `/backup/` directory on the backup server with the secure copy protocol (SCP).

2️⃣ Setup passwordless authentication between the app server and the backup server, so that it can access the backup server without requiring a password (as the operations are not going to be executed manually).

3️⃣ Gave the file execute permissions, so that it can be executed.

This way, the script can be run periodically by a cronjob to make the backup happen.

![Script result screenshot](<images/day-10 2025-08-14 095408.png>)