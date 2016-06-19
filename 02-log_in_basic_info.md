---
layout: default
title: Begginer Basic Info Login
---

#  Introduction

If you have recently created a DigitalOcean Droplet, and you are new to working with Linux servers, you will need to learn how to use SSH to connect to and manage it. SSH, which stands for Secure Shell, is an encrypted network protocol that is used to for, among other things, remote server login and command execution. It is the standard method used for accessing and interacting with Linux servers.

This quick tutorial will show you how to connect to your new Linux cloud server for the first time, by logging into it using an SSH client.

<h3>Prerequisites</h3>
The prerequisites section describes everything that you need know about to follow this tutorial. Of course, you will need to have created a new Droplet through the DigitalOcean Control Panel.

<br />

# Server Information and Login Credentials

In order to connect to a remote Linux server via SSH, you must have following:

`User name:` The remote user to log in as. The default admin user, or Superuser, on most Linux servers is root
Password and/or SSH Key: The password that is used to authenticate the user that you are logging in as. If you added a public SSH key to your droplet when you created it, you must have the private SSH key of the key pair (and passphrase, if it has one)

`Server IP address:` This is the address that uniquely identifies your server on the Internet, and can be found in your DigitalOcean Droplets page
If you did not add an SSH key to your Droplet when you created it, you should have received an email from DigitalOcean with the aforementioned connection information and credentials. The emailed password is temporary, and must be changed after the first login.
