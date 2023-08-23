# Ansible: Implementing Infrastructure as a Code
- ansible is a tool used for configuration management

## Useful Linux Commands
- Remove service from os:
``` sudo apt-get purge [arg] ```
- Add an Ansible role:
``` sudo ansible-galaxy init demo-nginx ```
- locally, the yml file (playbook) can be execute with command:
``` ansible-playbook nginx.yml --connection=local ```

## Course Content
1. Create your first infrastructure code using Ansible
2. Develop an Ansible playbook that starts Nginx service and enables it at boot time
3. Create handlers in Ansible that gets triggered only when a task is executed successfully and make changes in the server
4. Develop a reusable and modular infrastructure using Ansible roles
5. Create a complex Ansible role that customises our Nginx server

## Note on Infrastructure
- anything pertaining to configuration file, networks, or servers
- after cloud giant AWS introduced on 2002, instead of 10 can have thousands of servers
- infrastructure code in Ansible is written in yml files, aka playbooks

## Running Playbooks in Ansible
- locally, the yml file (playbook) can be execute with command:
``` ansible-playbook nginx.yml --connection=local ```

## Handlers and Notify
- task may need to be executed when a change has occurred in a machine
- if task updated configuration of particular service

## Roles
- a level of abstraction on top of task and playbooks
- can structure Ansible configuration in modular and reusable format
- useful for large complicated playbook file and have to divide it to multiple, smaller files
- automatically load variables files, handlers, and other Ansible artifacts
- Add an Ansible role:
``` sudo ansible-galaxy init demo-nginx ```
    * this will create a directory in /ansible/
    * created directory contains many folders
    * in "tasks" folder, there is a "main.yml" file

## Complex Roles
