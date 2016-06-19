---
layout: default
title: Log in to your droplet and Program Installations
---

# `1`.Create a Safe Account to Run Your Code

<h3>When you first set up your DigitalOcean droplet, you received instructions to log on using the root account. The instructions looked something like this:</h3>

To login to your droplet, you will need to open a terminal window
example.

* Lets use these keys to navigate quickly to our terminal
(`ctrl+alt+t`) and copy and paste the following string:`ssh root@ 123.456.78.90`

* Please note, '123.456.78.90' will be different for you.

  Follow the instructions you received from DigitalOcean when your virtual server was setup and log on using the terminal. If you run your code using the root account, and if a hostile party compromises the code, that party could get total control of your VPS (Virtual Private Server). To avoid this, let's setup a safe account that can still perform root operations if we supply the appropriate password.

  To get started, update your Ubuntu server by running the commands below. Assuming that you already have SSH with root access to the server, run the commands below to update your server.<br />
  `sudo apt-get update && sudo apt-get dist-upgrade && sudo apt-get autoremove`
  The one-line command above updates Ubuntu repositories, updates existing installed packages and removes unnecessary packages from your systems.

<h3>If the above info doesnt sound clear to then the following might be a good solution that will decrease your levels of uncertainties.</h3>[link]

<h3> Now Lets Install some programs that our apps are going to depend on.</h3>

* <h3>1.Install GIT</h3>

Once you have logged on, install GIT (we are going to use GIT to sync our work from github so our projects could exist on our digitalOcean cloud server which is our [VPS/Droplet] )

`sudo apt-get update && sudo apt-get install git`

The word sudo indicates that you want to run this command as root. You will be prompted for your password - i.e. the safe user password. When you provide your password, the command will run.
sudo apt-get update && sudo apt-get dist-upgrade && sudo apt-get autoremove
The one-line command above updates Ubuntu repositories, updates existing installed packages and removes unnecessary packages from your systems.

* <h3>2.Install MySQL</h3>

After installing Apache2, the next step is to install MySQL. The M in LAMP stands for MySQL and it’s a database server to host your website content.
To install MySQL, run the commands below.

`sudo apt-get install mysql-client mysql-server`

When you run the above commands, you’ll be prompted to create a database root password. Type and confirm one to continue.

* <h3>3.Install Nginx</h3>

<h2>OVERVIEW</h2>

Nginx (pronounced "engine x") is a free, open-source, high-performance HTTP server. Nginx is known for its stability, rich feature set, simple configuration, and low resource consumption. For these reasons, it is a great alternative to the more commonly used Apache web server.

Following the steps below will show you how to install Nginx and test its functionality. Be sure to follow our more advanced how-to on configuring virtual hosts afterwards, which will give you the ability to serve multiple websites from your (VPS) Server.

<h3>4.Install Nginx with command</h3>

`apt-get install Nginx`

By default, Nginx will not start automatically, so you need to use the following command. Other valid options are "stop" and "restart".
To restart we need to run the following command

 `sudo /etc/init.d/nginx start`

The results should be like the following.
Starting nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
configuration file /etc/nginx/nginx.conf test is successful
nginx.

`Test Nginx by pointing your web browser at your domain name or IP address. You should see the default Nginx page as shown in Figure 1 below: `


<!-- * <h3>5.Install Nodejs-legacy & NPM</h3>

Need install nodejs-legacy package ?

`sudo apt-get install nodejs-legacy.`

Then install npm:

`sudo apt-get install npm`. And right way to install Node.js:
`sudo apt-get install nodejs`

`sudo apt-get install nodejs-legacy`
`sudo apt-get install npm` -->
