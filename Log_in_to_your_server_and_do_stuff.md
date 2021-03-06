---
layout: default
title: Program Installation
---

<h3> Now Lets Install some programs that will enable you to run your Web Applications.</h3>

<h3>1.Install GIT</h3>

Once you have logged on, install GIT (we are going to use GIT to sync our work from github so our projects could exist on our digitalOcean cloud server which is our [VPS/Droplet] )

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo apt-get update && sudo apt-get install git`

The word sudo indicates that you want to run this command as root. You will be prompted for your password - i.e. the safe user password. When you provide your password, the command will run.
sudo apt-get update && sudo apt-get dist-upgrade && sudo apt-get autoremove
The one-line command above updates Ubuntu repositories, updates existing installed packages and removes unnecessary packages from your systems.

<h3>2.Install MySQL</h3>

After installing Apache2, the next step is to install MySQL. The M in LAMP stands for MySQL and it’s a database server to host your website content.
To install MySQL, run the commands below.

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo apt-get install mysql-client mysql-server`

When you run the above commands, you’ll be prompted to create a database root password. Type and confirm one to continue.

<h3>3.Install Nodejs & NPM</h3>

<h2>Install nodejs:</h2>
3.a)<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
 `sudo apt-get install nodejs` <br />

<h2>Then install npm:</h2>
3.b)<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
 `sudo apt-get install npm`


<h3>4.Install pm2</h3>

# Use NPM To Install A Package Called PM2.

Reminder. (NPM stands for - Node Package Manager ) and there are times when you will find deceiving meanings whereby people would say the NPM abbreviation stands for  (“No Problem Man”) .

NPM is a package manager that you will use to install frameworks and libraries to use with your Node.js applications. NPM was installed with Node.js. PM2 is a sweet little tool that is going to solve two problems for you:
It is going to keep your site up by restarting the application if it crashes. These crashes should NOT happen, but it is good know that PM2 has your back. (Some people may be aware of Forever.js, another tool that is used to keep node based sites running - I think you will find that PM2 has a lot to offer.)
It is going to help you by restarting your node application as a service every time you restart the server. Some of use know of other ways to do this, but pm2 makes it easier, and it has some added flexibility.
Install PM2 by typing the following at the command line:<br />

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo npm install pm2 -g`
<br />

<h3>5.Install Nginx</h3>

<h2>OVERVIEW</h2>

Nginx (pronounced "engine x") is a free, open-source, high-performance HTTP server. Nginx is known for its stability, rich feature set, simple configuration, and low resource consumption. For these reasons, it is a great alternative to the more commonly used Apache web server.

Following the steps below will show you how to install Nginx and test its functionality. Be sure to follow our more advanced how-to on configuring virtual hosts afterwards, which will give you the ability to serve multiple websites from your (VPS) Server.

<h3>Install Nginx with command</h3>

5.a)<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`apt-get install Nginx`

By default, Nginx will not start automatically, so you need to use the following command. Other valid options are `stop` and `restart`.
 To restart we need to run the following command:

 <input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
 `sudo /etc/init.d/nginx start`

<h3>The results should be like the following.</h3>

* `Starting nginx`:
 the configuration file /etc/nginx/nginx.conf syntax is ok
configuration file /etc/nginx/nginx.conf test is successful nginx.

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">`Test Nginx by pointing your web browser to your domain name or IP address. You should see the default Nginx page as shown in Figure 1 below: `

# Figure 1
![image-title-here](/img/posts_Schematics/Checkifnginxisinstalled.png){:class="img-responsive"}
