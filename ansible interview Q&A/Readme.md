* 1. What is Ansible, and what are its key features?
  Ansible is a configuration management tool. While working with Ansible, you can create various playbooks, inventory files, variable files, etc.
  Features:
  Agentless: Unlike Puppet or Chef, there is no software or agent managing the nodes.
  Python: Ansible is built on top of Python, which is easy to learn and write scripts. ...
  SSH: Passwordless network authentication makes it more secure and easy to set up.

* 2. How do you configure Ansible and nodes in a network environment?
  -->Install Ansible. ...
  -->Create an inventory by adding the IP address or fully qualified domain name (FQDN) of one or more remote systems to /etc/ansible/hosts . ...
  -->Verify the hosts in your inventory. ...
  Set up SSH connections so Ansible can connect to the managed nodes.

* 3.  Can you explain the concept of a playbook in Ansible?
    in ansible playbooks contains no.of plays and each plays contains no .of tasks and each task contains modules for installing and upgarding like etc...
* 4. What is configuration management, and how does Ansible facilitate it?
      
     configuration managementis  Controlling machine is where Ansible is installed and nodes are the ones that are managed by the controlling machines through SSH.


     There are a number of configuration management tools available on the market, with varying levels of complexity and diverse architectural styles. Although each of these tools have their own characteristics and work in slightly different ways, they all provide the same function: make sure a system’s state matches the state described by a set of provisioning scripts.

     Many of the benefits of configuration management for servers come from the ability to define your infrastructure as code. This enables you to:

     Use a version control system to keep track of any changes in your infrastructure
     Reuse provisioning scripts for multiple server environments, such as development, testing, and production
     Share provisioning scripts between coworkers to facilitate collaboration in a standardised development environment
     Streamline the process of replicating servers, which facilitates recovery from critical errors
     Additionally, configuration management tools offer you a way to control one to hundreds of servers from a centralized location, which can dramatically improve efficiency and integrity of your server infrastructure.

* 5. What is an inventory in Ansible, and how is it used?  
     Ansible works against multiple managed hosts in your infrastructure at the same time, using a list or group of lists is known as the inventory

     The Ansible inventory file defines the hosts and groups of hosts upon which commands, modules, and tasks in a playbook operate. The file can be in one of many formats depending on your Ansible environment and plugins.

     The simplest inventory is a single file with a list of hosts and groups. The default location for this file is /etc/ansible/hosts . You can specify a different inventory file at the command line using the -i <path> option or in configuration using inventory

* 6. explain the difference between static and dynamic inventory in Ansible?
      Static:A static inventory file is a plain text file containing a list of managed hosts or
      remote nodes whose numbers and IP addresses remain fairly constant. 
      Dynamic: On the other hand, a dynamic host file keeps changing as you add new hosts or 
      decommission old ones. 

* 7. What is Ansible Vault, and how is it used to secure sensitive information?

     Ansible Vault is an Ansible feature that helps you encrypt confidential information without compromising security. Ansible is a configuration management tool. While working with Ansible, you can create various playbooks, inventory files, variable files, etc.Some of the files contain sensitive and important data like usernames and passwords. Ansible provides a feature named Ansible Vault that prevents this data from being exposed. It keeps passwords and other sensitive data in an encrypted file rather than in plain text files. It provides password-based authentication.

* 8.  What is a Jinja template, and what is the difference between a template and a Jinja template in Ansible?
  
     Jinja2 templates are simple template files that store variables that can change from time to time. When      Playbooks are executed, these variables get replaced by actual values defined in Ansible Playbooks. This way, templating offers an efficient and flexible solution to create or alter configuration file with ease.

* 9. Which modules do you commonly use in your organization when working with Ansible?
      apt:
      repository
      file
      builtin
      adduser

* 10. Can you explain the concepts of roles, tasks, and handlers in Ansible?

     Handlers:In Ansible, handlers are typically used to start, reload, restart, and stop services. 
     Roles:Roles provide a framework for fully independent, or interdependent collections of variables, tasks, files, templates, and modules
     Tasks:he definition of an 'action' to be applied to the managed host. Tasks must always be contained in a Play, directly or indirectly (Role, or imported/included task list file).

* 11. How do you configure group inventory in Ansible?
      ```
      Step 1 — Creating a Custom Inventory File.
      Step 2 — Organizing Servers Into Groups and Subgroups.
      Step 3 — Setting Up Host Aliases.
      Step 4 — Setting Up Host Variables.
      Step 5 — Using Patterns to Target Execution of Commands and Playbooks.
      ```

* 12. What are modules in Ansible, and how are they used? 
      A module is a reusable, standalone script that Ansible runs on your behalf, either locally or remotely.      
      Modules interact with your local machine, an API, or a remote system to perform specific tasks like changing a database password or spinning up a cloud instance.

* 13. Can you provide an overview of Ansible Collections and their significance?      
      Ansible Content Collections represent the new standard for distributing, maintaining, and using automation. It combines multiple types of Ansible Automation Platform content, improving flexibility and scalability.

* 14. How do you pass values dynamically when running a playbook in Ansible
     ansible playbook -e hosts_vars hosts playbook/yaml<keyvaluepair>


