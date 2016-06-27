---
layout : default
title : UWF - Uncomplicated Firewall configuration
---

# UFW (Built-in component)

<h3>On Linux-based-operating System UFW is always installed by default</h3>

*  note. You can run both commands nothing could go wrong. We hope you are going to notice something!:grinning:

<h3>How to check if UFW is installed?</h3>
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`apt-cache policy ufw`

<h2>OR</h2>

<h3>Use check installed program version?</h3>
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`ufw --version`

#  Lets introduce the default firewall configuration tool for Ubuntu

`UFW`, or `Uncomplicated Firewall`, is an interface to [iptables](/glossary/iptables.html). that is geared towards simplifying the process of configuring a firewall. While iptables is a solid and flexible tool, it can be difficult for beginners to learn how to use it to properly configure a firewall. If you're looking to get started securing your network, and you're not sure which tool to use, UFW may be the right choice for you.

# Prerequisites
Before you start using this tutorial, you should have a separate, non-root superuser account—a user with sudo privileges—set up on your Ubuntu server. You can learn how to do this by completing at least steps 1-3 in the Initial Server Setup with Ubuntu 14.04 tutorial.
UFW is installed by default on Ubuntu. If it has been uninstalled for some reason, you can install it with apt-get:
sudo apt-get install ufw


# Using IPv6 with UFW

If your Ubuntu server has [IPv6](/glossary/ipv4andipv6info.html). enabled, ensure that UFW is configured to support IPv6 so that it will manage firewall rules for IPv6 in addition to IPv4. To do this, open the UFW configuration with your favorite editor. We'll use nano:

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo nano /etc/default/ufw`


<h3>Then make sure the value of "IPV6" is to equal "yes". It should look like this:</h3>

/etc/default/ufw excerpt


...<br />
IPV6=yes
<br />
...

<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">Save and quit.

 Hit Ctrl-X to exit the file, then Y to save the changes that you made, then <input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">`ENTER` to confirm the file name.


When UFW is enabled, it will be configured to write both IPv4 and IPv6 firewall rules.
This tutorial is written with IPv4 in mind, but will work fine for IPv6 as long as you enable it.


# :eyes: Check UFW Status and Rules :eyes:

At any time, you can check the status of UFW with this command:
`sudo ufw status verbose`
By default, UFW is disabled so you should see something like this:
<h3>Output:</h3>

`Status: inactive`

If UFW is active, the output will say that it's active, and it will list any rules that are set. For example, if the firewall is set to allow SSH (`port 22`) connections from anywhere, the output might look something like this:

<h3>Output:</h3>
<pre><code>Status: active
Logging: on (low)
</code></pre>

<h3>Default:</h3> deny (incoming), allow (outgoing), disabled (routed)
New profiles: skip
<pre><code>To           Action      	From
--            ------     	----
22/tcp        ALLOW IN   	 Anywhere
</code></pre>

# Configuring a Basic Firewall

Firewalls provide a basic level of security for your server. These applications are responsible for denying traffic to every port on your server with exceptions for ports/services you have approved.


Before we enable or reload our firewall, we will create the rules that define the exceptions to our policy. First, we need to create an exception for SSH connections so that we can maintain access for remote administration.


The SSH daemon runs on port 22 by default and ufw can implement a rule by name if the default has not been changed. So if you have not modified SSH port, you can enable the exception by typing:<br />
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo ufw allow ssh`


If you have modified the port that the SSH daemon is listening on, you will have to allow it by specifying the actual port number, along with the TCP protocol:<br />
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox">
`sudo ufw allow 4444/tcp`

This is the bare minimum firewall configuration. It will only allow traffic on your SSH port and all other services will be inaccessible. If you plan on running additional services, you will need to open the firewall at each port required.
