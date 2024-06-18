---
 layout: post
 title: DAY SEVEN AT COREDGE
 date: 2024-6-12
---
**2024-6-12- AS A LINUX ADMIN**

On day seven i have learned about ansible and how ansible works
and also learned abou ansible playbook which is written in yaml format..

**What is Ansible?** 

Ansible is simply an open-source IT engine that automates application deployment, intra service 
orchestration, cloud provisioning, and many other IT tools. 
 
Ansible is easy to deploy because it does not use any agents or custom security infrastructure.

**Advantages of Ansible**

**Free**
**Agentless**
**Very simple to set up and use**
**Flexible**
**Powerfull**

**What is Configuration Management?**

Configuration management in terms of Ansible means that it maintains the configuration of the product 
performance by keeping a record and updating detailed information that describes an enterprise’s 
hardware and software.


**Ansible - Environment Setup**
 
**Installation Process**

Mainly, there are two types of machines when we talk about deployment − 

 Control machine − Machine from where we can manage other machines. 

 Remote machine − Machines that are handled/controlled by the control machine. 

There can be multiple remote machines that are handled by one control machine. So, for managing 
remote machines we have to install Ansible on the control machine. 
 
Control Machine Requirements 
Ansible can be run from any machine with Python 2 (versions 2.6 or 2.7) or Python 3 (versions 3.5 and 
higher) installed. 

Note − Windows does not support a control machine. 
By default, Ansible uses ssh to manage a remote machine. 
Ansible does not add any database. It does not require any daemons to start or keep it running. While 
managing remote machines, Ansible does not leave any software installed or running on them. Hence, 
there is no question of how to upgrade it when moving to a new version. 
Ansible can be installed on the control machine which has the above-mentioned requirements in 
different ways. You can install the latest release through Apt, yum, pkg, pip, OpenCSW, Pacman, etc. 

1- Add user on each machine named for example (Ansible) 
2- Configure SSH login between these servers (control and remotes) without a password  
3- Install Ansible:  

[root@ansible-control ~] # yum install -y ansible 

After running the above line of code, you are ready to manage remote machines through Ansible. Just 
run Ansible --version to check the version and just to check whether Ansible was installed properly or 
not.


**Ansible - YAML Basics**
 
Ansible uses YAML syntax for expressing Ansible playbooks. This chapter provides an overview of YAML. 
Ansible uses YAML because it is very easy for humans to understand, read and write when compared to 
other data formats like XML and JSON. 
Every YAML file optionally starts with “---” and ends with “...”. 

**Understanding YAML** 

In this section, we will learn the different ways in which the YAML data is represented. 

key-value pair 

YAML uses simple key-value pairs to represent the data. The dictionary is represented in key: value pair. 

Note − There should be space between: and value. 

Example: A student record

--- #Optional YAML start syntax  
james:  
   name: james john  
   rollNo: 34  
   div: B  
   sex: male  
… #Optional YAML end syntax 

**Here we are going to install some services on worker's machines..**

---
# This is a simple playbook with two plays
- name: First play
 hosts: web.example.com
 tasks:
 - name: First task
 ansible.builtin.dnf:
 name: httpd
 status: present
 - name: Second task
 ansible.builtin.service:
 name: httpd
 enabled: true
- name: Second play
 hosts: database.example.com
 tasks:
 - name: First task
 ansible.builtin.service:
 name: mariadb
 enabled: true
