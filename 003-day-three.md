# 🗓️ Day 3 / 100

100 Days of DevOps

Today's task was to disable root login through SSH. Allowing people to login as root over SSH connections makes it harder to track who did what. It also just increases the possibility of catastrophic mistakes, as the root has permissions and can really edit any file.

This is done by editing the `/etc/ssh/sshd_config` file and changing `PermitRootLogin yes` to `PermitRootLogin no`.

I initially made the mistake of not restarting the sshd daemon after editing the config file. And that caused me to fail and redo the task.

![](<images/day-3 2025-08-07 070729.png>)
