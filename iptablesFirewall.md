# How the Iptables Firewall Works

# Introduction

Setting up a good firewall is an essential step to take in securing any modern operating system. Most Linux distributions ship with a few different firewall tools that we can use to configure our firewalls. In this guide, we'll be covering the iptables firewall.

Iptables is a standard firewall included in most Linux distributions by default (a modern variant called nftables will begin to replace it). It is actually a front end to the kernel-level netfilter hooks that can manipulate the Linux network stack. It works by matching each packet that crosses the networking interface against a set of rules to decide what to do.

In this guide we will discuss how iptables works. In the next article in the series, we'll show you how to configure a basic set of rules to protect your Ubuntu 14.04 server.
