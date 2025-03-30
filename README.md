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
