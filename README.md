# Ansible
This repository will discuss about Ansible, Ad-hoc commands, Playbooks, Roles and Anible galaxy:

Ansible is a multiplier, a tool that automates and scales infrastructure of every size. 

It is considered to be a configuration management, orchestration, and deployment tool.

Ansible automates using the SSH protocol. The control machine uses an SSH connection to communicate with its target hosts, which are typically Linux hosts. 
If you’re a Windows sysadmin, you can still use Ansible to automate your Windows environments using WinRM as opposed to SSH. 

What Ansible does?

Common sysadmin tasks that can be performed with Ansible include patching, updating systems, user and group management, and provisioning.
Ansible presently has a huge footprint in IT Automation—if not the largest presently—and is considered to be the most popular and widely used configuration management, orchestration, and deployment tool available today.

Ansible uses YAML (Yet Another Markup Language) in its configuration and automation jobs which are human-readable and quite easy to follow. YAML uses SSH protocol to communicate with remote servers, unlike other automation platforms that require to you install an agent on remote nodes to communicate with them.

A playbook is a set of instructions which is called as task or play that define how tasks are to be executed on remote hosts or a group of host machines. 

- Playbooks: A List of plays.
- Plays: Task.
- Task: Invoking the ansible module.

Ansible Roles:

In Ansible, the role is the primary mechanism for breaking a playbook into multiple files. This simplifies writing complex playbooks, and it makes them easier to reuse. The breaking of playbook allows you to logically break the playbook into reusable components.

Roles are not playbooks. Roles are small functionality which can be independently used but have to be used within playbooks. There is no way to directly execute a role. Roles have no explicit setting for which host the role will apply to.

![image](https://user-images.githubusercontent.com/41946619/109410404-77788180-79c0-11eb-9663-115d6a92c011.png)


Here:
- tasks/main.yml - the main list of tasks that the role executes.

- handlers/main.yml - handlers, which may be used within or outside this role.

- library/my_module.py - modules, which may be used within this role.

- defaults/main.yml - default variables for the role. These variables have the lowest priority of any variables available, and can be easily overridden by any other variable, including inventory variables.

- vars/main.yml - other variables for the role.

- files/main.yml - files that the role deploys.

- templates/main.yml - templates that the role deploys.

- meta/main.yml - metadata for the role, including role dependencies.

Ansible Galaxy:

Ansible Galaxy is essentially a large public repository of Ansible roles. Galaxy contains a large number of roles that are constantly evolving and increasing.

Galaxy can use git to add other role sources, such as GitHub. You can initialize a new galaxy role using ansible-galaxy init, or you can install a role directly from the Ansible Galaxy role store by executing the command ansible-galaxy install <name of role>.

Here are some helpful ansible-galaxy commands you might use from time to time:
    
-  ansible-galaxy install <name of role>. #It installs one or more connections.
-  ansible-galaxy list  #displays a list of installed roles, with version numbers.
-  ansible-galaxy remove <role> # Removes an installed role.
-  ansible-galaxy info  #Provides a variety of information about Ansible Galaxy.
-  ansible-galaxy init nginx_ansible #It creates a basic collection Skeleton based on the default template included with Ansible or your own template.
-  ansible-galexy build #It creates a collection artifact that can be uploaded to the galaxy or your own repository.
-  ansible-galexy publish #It publishes a built connection artifact to the galaxy.
  
The Keys Features of Ansible
- Agentless
- Idempotent
- Simple and extensible
