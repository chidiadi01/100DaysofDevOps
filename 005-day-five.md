# 🗓️ Day5/100

100 Days of DevOps

Today's task was to install SELinux packages. SELinux or Security-Enhanced Linux is a Linux kernel security module (LSM) that prodivdes enhanced security for Linux systems through Mandatory Access Control (MAC) instead of the traditional Dicretionary Access Control (DAC) where the owner of the file really decides, at his discretion, what permissions are granted.

With MAC, access decisions are enforced by the system based on predefined security policies, not just file ownership or standard permissions.
SELinux policies make use of users, roles, and domains. It’s like Role-Based Access Control (RBAC) for Linux, where processes and users are confined to specific domains and roles. This way, even if a process is compromised, it can only access the resources its policy explicitly allows.

SELinux can greatly limit the damage from security breaches by restricting what a compromised service or process can do, regardless of the privileges of the account it runs under.

![Installations complete](<images/day-5 2025-08-09 073613.png>)