## Jenkins ansible playbooks
A collection of playbooks to install:

* Oracle JDK 1.8
* Jenkins server 2.75 with required plugins (blue ocean by default)

### Requirements

* Vagrant 1.9.7
* VirtualBox 5.1.22
* Ansible 2.3.2.0


### How to run

* install required roles

      ansible-galaxy install -r requirements.yml

* provision a VM and apply playbooks

      vagrant up
      
### How to backup Jenkins
     
* backup Jenkins configuration from VM to localhost
       
       ansible-playbook backup-jenkins.yml -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory -vv --extra-vars "command=pull"

* restore Jenkins configuration from localhost to a VM    

       ansible-playbook backup-jenkins.yml -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory -vv --extra-vars "command=push"

### Tips

Sometimes you may need to increase access permissions to /var/lib/jenkins after restoring a backup to a VM


