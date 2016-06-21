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

# SSH Client Software

There are a variety of SSH clients that you can use to connect to a Linux server. We will cover the following two:

OpenSSH (Linux and Mac OS X): A collection of software that ships with most Unix-like operating systems that includes the ssh command
PuTTY (Windows): A free SSH client that can run on Windows, and is available for download on the PuTTY Download Page. putty.exe is the SSH client, and puttygen.exe should also be downloaded if you want to use SSH keys.

# SSH Login as Root

Now that you have all of the required information and software, you are now ready to log in to your server for the first time. Make sure to only follow the instructions that are relevant to your SSH client.

# Option 1: OpenSSH (Linux and Mac OS X)

<h3>The OpenSSH ssh client is a command-line tool, so open a Terminal window to get started.</h3>

<h3>Step 1 — Initiate the Connection</h3>

At the command prompt, enter the following command to attempt to connect to your server as the root user
<br />
(subsitute the highlight word(*SERVER_IP_ADDRESS*) with your server's IP address):

`ssh root@SERVER_IP_ADDRESS`

For example, if the server IP address was `123.456.789.123`, the command would look like this:<br />
$<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`ssh root@123.456.789.123`

<h3>The first time you attempt to connect to your server, you will likely see a warning that looks like this:</h3>

$`The authenticity of host '123.123.123.123 (123.123.123.123)' can't be established.
ECDSA key fingerprint is 79:95:46:1a:ab:37:11:8e:86:54:36:38:bb:3c:fa:c0.Are you sure you want to continue connecting (yes/no)?`

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
Go ahead and type `yes` to continue to connect.

* Here, your computer is telling you that the remote server is not recognized. Since this is your first time connecting, this is completely expected. Skip to step 2, Authentication.

If you happened to destroy a droplet directly prior to creating the one that you are connecting to, you may see a warning like this:

<pre><code>@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@</code></pre>
* IT IS POSSIBLE THAT SOMEONE IS DOING SOMETHING NASTY!
<br />
<p>Someone could be eavesdropping on you right now (man-in-the-middle attack)!
It is also possible that a host key has just been changed.
...</p>
If this is the case, your new droplet probably has the same IP address as the old, destroyed droplet, but a different host SSH key. This is fine, and you can remove the warning, by deleting the old droplet's host key from your system, by running this command:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`ssh-keygen -R SERVER_IP_ADDRESS`
Now try connecting to your server again.


<h3>Step 2 — Authenticate</h3>

* The authentication step involves providing a password and/or a private SSH key to prove that you are authorized to log in as root.

If you added an SSH key to your Droplet, and you have the private key installed on your computer, OpenSSH will attempt to use the key to authenticate to the root account. If you used a key with a passphrase, you will need to provide the passphrase to complete the login process. At this point, if you are unable to log in, you may need to start your ssh-agent and add your SSH keys to it with the following command (assuming your key is called "id_rsa"), then go back to Step 1:

eval `ssh-agent -s`

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`ssh-add ~/.ssh/id_rsa`
If you did not add an SSH key to your Droplet, you will be prompted for the temporary password, and you will also be required to change it. Follow these steps to complete the login process:

Copy the temporary password from the email, and paste it into the password prompt
At the (current) UNIX password prompt, paste in the temporary password again
At the Enter new UNIX password prompt, enter a strong password
At the Retype new UNIX password prompt, enter the same strong password that you just entered.
