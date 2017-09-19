## Ansible
Ansible is configuration management, software provisining tool. 

## Ansible Functions 

**1. Change Management**

**2. Provisioning**

**3. Automation**

**4. Orchestration**

**Change Management**-When the system is deviated from the state is called change. For production system changing the system state is crucial. Is should change unless there is a requirements. 

**Provisioning**-Provisioning is transition from one state to a different state. It's like prepare a system to make it ready. It's like installing software on the machine. Ansible sends step by step command to the server to set up and configure the server.

**Automation**-Ansible is automation tool, if break the functionality of ansible, we find automation at lower level. We can also say that define task to be executed automatically. Ansible is used for adhoc tasks and logic control what to run and when to run. Ansible make the automation easy.

**Orchestration**- Automation take place on single system, whereas Orchestration takes automation to multiple server and cordination

**YAML**- No programming required, not a MARK UP language. It is structured. Easy to read and write. 

Ansible works on built in security system SSH. 

**Easy to extend**

URL / RESTful Calls

Shell Commands 

Scripts

Asible-Galaxy - Community bases catalogue. 

## Components of Ansible

**Inventory-** A text file where we can define host level variables. 

**Playbook-** Playbooks are text/yaml file where define the individual task, like  individual play. We buid are automation or orchestration using play-books files and playbook command. A set of plays built in specific orders sequence to produce an expected outcome and outcomes across many set of different hosts.

**Modules-** Modules have modules which needs to be performed on different hosts. A programmed unit of work to be done. Suppose we want to install some software on Red Hat, Cent OS then use `yum` module. If we want to install some software on debian then use `apt` module.

**Play-** A single or set of tasks using modules, executed on a defined set of hosts.  

**Ansible config-** This contains global set of variables and allows you to change it's defaults. 

**Python-** Ansible takes all those componets and push through python components, using python it also helps in building variables.

## Variables in ansible
**1. Host Variables** Use variables defined in inventory per host or group.

**2. Facts Variables** Use data from the remote managed host like IP, Memory and even if you want CPU speed.

**3. Dynamic Variables** Use data gathered by tasks or created at run time.



