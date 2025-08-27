# 🗓️ Day 1/100

I started the 100 Days of DevOps challenge by KodeKloud. The task was simple: to create a Linux user with a non-interactive shell.

A non-interactive shell is a shell that does not receive input from the user (STDIN is not attached). It does not expect input, though the STDOUT and STDERR can still be attached to the terminal, so it can output logs and errors. It just runs a command or process.

An example is docker. When you run a docker container with a bash command passed into it (`docker run ubuntu bash -c "ls"`), it just spins up a new shell and runs, and you can't talk to it. Hence, the `-i`  and `-t` flags to make it accept your input and behave like a normal terminal. Cronjobs and bash scripts also run in non-interactive shells. They don't exoect you to give any more commands in the middle of the process.

To create a non-interactive user, you just have to add this flag that tells Linux the shell should be `/sbin/nologin`, a program that exits immediately and does not allow user to login.

`sudo useradd -s /sbin/nologin chidiadi-service`

Such a user cannot login, but can still own files and be used to run a service.

![](<images/day-1 2025-08-05 214517.png>)