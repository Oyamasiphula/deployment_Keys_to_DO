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


Then make sure the value of "IPV6" is to equal "yes". It should look like this:
