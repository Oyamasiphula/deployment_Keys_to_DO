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
