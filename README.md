## Jenkins ansible playbooks
A collection of playbooks to install:

* Oracle JDK 1.8
* Jenkins server 2.75 with required plugins

### Requirements

* Vagrant 1.9.7
* VirtualBox 5.1.22
* Ansible 2.3.2.0


### How to run

* install required roles

      ansible-galaxy install -r requirements.yml

* provision a VM and apply playbooks

      vagrant up
    
    


