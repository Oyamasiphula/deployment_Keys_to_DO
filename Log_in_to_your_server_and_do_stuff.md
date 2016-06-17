---
layout: default
title: Log in o your droplet and Program Installations
---


# `1`.Create a Safe Account to Run Your Code


<h3>When you first set up your DigitalOcean droplet, you received instructions to log on using the root account. The instructions looked something like this:</h3>

To login to your droplet, you will need to open a terminal window
example.

* Lets use these keys to navigate quickly to our terminal
(`ctrl+alt+t`) and copy and paste the following string:`ssh root@ 123.456.78.90`

* Please note, '123.456.78.90' will be different for you.

  Follow the instructions you received from DigitalOcean when your virtual server was setup and log on using the terminal. If you run your code using the root account, and if a hostile party compromises the code, that party could get total control of your VPS (Virtual Private Server). To avoid this, let's setup a safe account that can still perform root operations if we supply the appropriate password.
