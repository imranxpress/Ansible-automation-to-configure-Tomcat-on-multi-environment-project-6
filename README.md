# Ansible-automation-to-configure-Tomcat-on-multi-environment-project-6


## Table of Contents

   ### 1. Goal
   ### 2. Pre-Requisites
   ### 3. Automation
   ### 4. Validation
   ![aws-7](https://user-images.githubusercontent.com/47071968/229018605-7c2b46eb-3632-4180-8cae-1e96121b37aa.jpeg)


## Goal

Goals of this project to automate Tomcat application server deployment on multi environment – Dev & Prod.
   


## Pre-Requisites

    1. Install Ansible control engine on development platform.
    2. Install Visual Code on development platform.
    3. Deploy Ansible Control Node, Dev Application server & Prod Application Server as per the above architecture.
    
  ##  Automation


   Develop Ansible Role to provision tomcat application server on target environment as per below configuration

   1. Install common dependencies AWS-CLI, wget, curl, git
   2. Install Java 11
   3. Download and install tomcat into CATALINA HOME  ‘/usr/local/tomcat’
   4. Configure systemd service to manage ‘tomcat’ service.
   5. Configure tomcat user ‘admin’ and assign manager & admin role access.
   6. Integrate Ansible vault to store the tomcat user ‘admin’ passwords.
   7. Restart Apache tomcat service only when tomcat configuration file changes.


## Validation

   1. Run Ansible Playbook to invoke the Role and configure the Dev environment
   2. Run Ansible Playbook to invoke the Role and configure the Prod environment
   3. Access Tomcat page using curl from Ansible control node.

Note:  Goal is to achieve the desired configuration on target nodes, this project not listed any specific best practices to follow, But recommended to apply variables, secure passwords, handlers, custom inventory path etc..
