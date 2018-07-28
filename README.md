# ansible-hortonwork-hadoop-stack

This repository contains the configurations to install 12 nodes Hortonworks Data Platform (HDP) cluster and setup 3 High-Available Masters using the ansible roles developed Hortonworks. 

## Blueprint
![blueprint](https://github.com/kc-cloud/ansible-hortonwork-hadoop-stack/blob/master/blue-print.png)
## Prerequisite
* Ansible roles and playbooks developed by  Hortonworks (https://github.com/hortonworks/ansible-hortonworks)
* pre-installed MySQL database

## Tested platforms:
Tested in the following Operating systems in the Google Cloud Platform
* CentOS Linux 7.5

## Steps to configure and execute ansible playbooks:
   * download the repository from https://github.com/hortonworks/ansible-hortonworks.git 
   * modified ansible-hortonwork-hadoop-stack/inventory/static to add the 12 nodes (as given in this repository)
   * modified ansible-hortonwork-hadoop-stack/playbooks/group_vars/all.yml (as given in this repository) to add version details
   * added ansible-hortonwork-hadoop-stack/playbooks/group_vars/ambari-server.yml for the ansible to generate ambari blueprint
   * follow the steps given in the https://github.com/hortonworks/ansible-hortonworks/blob/master/INSTALL_static.md
