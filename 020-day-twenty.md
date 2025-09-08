# 🗓️ Day 20 / 100

100 Days of DevOps 🚀 

🔴 TASK: Setup nginx and PHP-FPM using Unix sock

First of all, I don't know much about PHP, but when I did a little research, I found out that Nginx cannot run PHP processes, so it needs to pass on PHP traffic to a service that can spin up PHP processes and process requests, and that's where Fast CGI Process Manager comes in.

Setting up this involved:

✅ Installing Nginx

✅ Installing the right version of PHP-FPM as required in the exercise

✅ Configuring PHP-FPM to use the specified socket

✅ Configuring an HTTP upstream block to the PHP-FPM  socket

## 🧿 INSTALLING PHP-FPM

To install PHP, I first checked the PHP streams available with the default package repositories with `dnf module list php`.

![Module list screenshot](<images/day-20 2025-09-08 175328.png>)

Then I reset the modules and enabled the stream of the version of PHP I was meant to install with `sudo dnf module reset php -y` and `sudo dnf module enable php:8.1`.

Then I installed PHP-FPM and it installed the corresponding version.

## 🧿 CONFIGURING PHP-FPM

I had to setup PHP-FPM to listen at a specified socket. First of all, I made sure the directory existed and had enough permissions. Then I went to the `/etc/php-fpm.d/www.conf` file and searched for 'listen'. I added the socket directory there, and also uncommented the permissions under it. I set them to nginx, even though I didn't set the actual directory to be owned by nginx. I just left it at root.

## 🧿 CONFIGURING NGINX

I didn't go to the main nginx config file `/etc/nginx/nginx.conf`. I rather created a different file under the `/etc/nginx/conf.d` directory that was included in the main config file. I specified a `server` block there. There was actually another file in that directory with an upstream context for the PHP-FPM. I changed the socket in there to the one I used in the PHP-FPM configuration.

## 🧿 WRAPPING UP

I then restarted both services, and checked to see that the site was accessible from the jumphost.

I guess I'm beginning to write full articles here. 😂 

![Final screenshot](<images/day-20.png>)