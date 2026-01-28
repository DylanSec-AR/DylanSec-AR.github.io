---
layout: post
title: OS Transitions and Virtual Machine Setups for Enhanced Flexibility
date: 2026-01-25 15:16:00
description: Security through isolation and flexibility are some pros of using virtual machines
tags: virtualization software
categories: Portfolio
pseudocode: true
---
Exploring operating systems has been a key part of my self-learning. 
I recently migrated my laptop from Windows to Linux Mint, a process involving backing up data, creating a bootable USB via Rufus, partitioning the drive with GParted, and configuring GRUB for dual-boot.
This switch improved system stability and introduced me to open-source tools like apt for package management. 
Building on that, I set up a virtual environment using VirtualBox, provisioning three VMs: Windows 7 for legacy software testing, Windows XP to simulate outdated environments, and Kali Linux for penetration testing exercises from my cybersecurity studies.
I allocated resources (1gb for xp, 2 RAM for win7, 4 for kali linux), networked them (internal networks, isolated), and installed tools like Metasploit in Kali. 
This setup allowed safe experimentation, such as testing malware in isolation.
<div class="row justify-content-center">
    <div class="col-md-8"> {% include figure.liquid path="assets/img/LAB-DYLAN12.png" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">
    After networking them the only thing left was to test it by trying to reach the other virtual computers. I did this with the Kali Linux CLI, by: 
<ul>
  <li>typing "ping 192.168.10.1" and "ping 192.168.10.3" respectively, this command uses ICMP protocol (TCP/IP internet layer).</li>
  <li>typing "ip neigh". This command checks the ARP table to see past connections and gives data about its state (e.g. REACHABLE, STALE, FAILED)</li>
  <li>typing nmap "-sV 192.168.10.1" and "-sv 192.168.10.3". Nmap is a reconaissance tool that scans for open ports by manipulating TCP handshake process</li>
</ul>
</div>
