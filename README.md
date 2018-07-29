# ansible-hortonwork-hadoop-stack

This repository contains the configurations to deploys 12 nodes Hortonworks Data Platform (HDP) cluster and setup 3 High-Available Masters using the ansible roles developed by Hortonworks. Installation contains:

* ambari_version: '2.5.2.0'
* hdp_version: '2.6.2.0'
* hdf_version: '3.0.1.1'


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
   * modified _ansible-hortonwork-hadoop-stack/inventory/static_ to add the 12 nodes (as given in this repository)
   * modified _ansible-hortonwork-hadoop-stack/playbooks/group_vars/all.yml_ (as given in this repository) to add version details
   * added _ansible-hortonwork-hadoop-stack/playbooks/group_vars/ambari-server.yml_ for the ansible to generate ambari blueprint
   * follow the steps given in the https://github.com/hortonworks/ansible-hortonworks/blob/master/INSTALL_static.md
