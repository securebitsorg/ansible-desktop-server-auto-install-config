> [!IMPORTANT] 
> # PLEASE NOTE !!!
> First, the Ansible configs must be adapted to your needs. For example, the “Users”, “Devices”, “Groups”, “Packages”, etc.
> 
> This Ansible-Config is adapted to my personal setup :-)

# Ansible Desktop Configs

If you want to use Ansible to automatically set up all your workstations, laptops and servers, then this Ansible script repository will help you automate your installation.

## !!! Info !!!

**Please do not execute this repository directly on your servers, workstations and laptops!
First, you have to customize these config files to your environment. How this works, you can read in the respective “Readme.md” in each directory.**

## Structure of this repository

This is how the folder structure is organized:

### local.yml: 
This is where you'll find the “index” for the pull via Git for your Ansible config.

### ansible.cfg:
This is where you will find the instructions for configuring Ansible.

### group_vars:
Here you have the option to store the variables you want to use on each system.

### host_vars:
You can store your servers, desktops and laptops here via hostname.

### hosts:
This is where the “Inventory File” is located, where you can store your devices and sort them into the groups accordingly.
Example: 

[server]
server1.mydomain.com
[workstation]
workstation1.mydomain.com
[laptop]
laptop1.mydomain.com

### playbooks
You can store further playbooks here that you would also like to execute.

### roles:
This directory contains my base, workstation and server roles. Each host is assigned the base role. Then either “workstation” or “server”, depending on what it is intended for.

### roles/base:
This role is intended to roll out recurring configurations that are the same on all systems. For example, user roles, etc.

### roles / workstation:
This role determines how all desktops/laptops are to be configured. For example, the GUI configuration, packages to be installed, and so on...

### roles / server
This role is similar to the previous one and is designed to configure the corresponding server systems.


## Special thanks go to:

 !!! **LearnLinuxTV** !!!, thanks to the example config from Jay (LearnLinuxTV), I was inspired to dedicate myself to this project here and to adapt it to my needs.
For those of you who want to learn Ansible, I can only recommend the playlist for Ansible from this channel!
You can find the playlist here:

https://youtu.be/3RiVKs8GHYQ?si=_2j3P9oWI25jBDIz