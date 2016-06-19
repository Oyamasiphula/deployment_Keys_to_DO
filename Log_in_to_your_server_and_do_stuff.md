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

<h3>If the above info doesnt sound clear to then the following might be a good solution that will decrease your levels of uncertainties.</h3>
