# 🗓️ Day 7 /100

100 Days of DevOps

Today's task was to setup passwordless authentication with SSH. SSH is a very common protocol, and way of logging into remote servers and network devices. It enables you to access their terminals from your machine.

The process of setting up this passwordless authentication involves generating an SSH key pair (public and private keys), and then copying the public keys to the server you want. In this case, I used the same public keys for the three servers.

This was done with CLI, but there are also GUI tools for doing this, like PuTTY – which I have used in the past, SecureCRT, Termius, and MobaXterm. But before SSH was telnet. And I once wrote an article explaining the origin of remote access to machines through the terminal. In that article, you can also see where the terms TTY and CRT came from, and how they're associated with remote access of machines through terminals.

Here is the article: https://www.linkedin.com/pulse/common-nameless-network-protocol-chidiadi-anyanwu/

![](images/day-7%202025-08-11%20085106.png)