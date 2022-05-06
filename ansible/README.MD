## Ansible Source Code & Examples 

In this training module you will find source code & examples for inventorys, playbooks, ansible roles, handlers and tests. 

## Requirements
For the basic examples you need only a local or remote machine with the required tools installed. If you are going forward to the more mature stuff you need to fullfill the additional tool section as well.

required tools :
- git
- ansible

additional tools:
- jenkins
- molecule

We would recommend to have a target host for the installation task, but it would be also possible to use the plays local.

## Usage
Navigate from your `infra_automation` directory  to the `ansible` directory. From this point you can switch to *_example and execute the ansible commands.

The environment will be spawned every day. So you need to check the [Inventory](../inventory)

You need to find the following informations:
- jenkins
- name_student-centos-{n - 1}

Connect to the Jenkins server ip with ssh (via MobaXterm f.e.).
- user: student-{n}
- ssh-key: student-{n}

You could reach you student machine `name_student-centos-{n - 1}` via ssh as well with:
- user: student-{n}
- ssh-key: student-{n}

If you are connected the Jenkins server you could check out the Code:
```
[student-2@ip-172-31-35-110 ~]$ eval $(ssh-agent)
Agent pid 87022
[student-2@ip-172-31-35-110 ~]$ ssh-add ~/.ssh/bitbucket
Identity added: /home/student-2/.ssh/bitbucket (/home/student-2/.ssh/bitbucket)
```
Switch to your project project directory:
```
cd infra_automation
git clone ssh://git@innersource.accenture.com/asgiac/spring.automation.bootcamp.git
```

### inventory_example

The inventory_examples will give you only an idea, on how to structure your inventory and what can be done. To execute this example for your own, you need a few target hosts and build up your own inventories.

To try this examples connect to the Jenkins with MobaXterm. Go to the [Inventory](../inventory) and build your own inventory.

An Example which will work on both student and Jenkins server is the follow:
```
cd ansible/variables_example

ansible-playbook -i ../inventory_examples/local_inventory -c local gather_facts.yaml 
```

### variables_example

In this section you will find different examples for variables and playbook steps. To execute the playbook use the following example:

Connect yourself to the student server `name_student-centos-{n - 1}` and checkout the code from the Automation Bootcamp as described before.

Gather Facts from the local system:
```
cd ansible/variables_example

ansible-playbook -i "localhost," -c local gather_facts.yaml 
```

Some examples are only ansible related and don't do anything on your local system. In some playbooks you will do some installation tasks on your system. We have added the manual installation steps, so that you know what happens in the playbook.

1. handler.yaml

Install a webserver with the dnf package manager.
```
#sudo dnf install -y httpd
```

Restart the webserver.
```
#sudo systemctl restart httpd.service
```

2. handler_change_index.yaml

Install a webserver with the dnf package manager and create a index.hmtl file which will be presented to us. After that the restart will be done.
```
#sudo dnf install -y httpd
#echo "This is Sebastian index.html file for $(hostname)"
#sudo systemctl restart httpd.service
```

3. install_packages_wo_loop.yaml
Install a webserver, terminal multiplexer and texteditor with the dnf package manager.
```
#sudo dnf install -y httpd
#sudo dnf install -y tmux
#sudo dnf install -y vim
```

### playbook_example

In this section you will find different examples for variables and playbook steps. To execute the playbook use the following example:

Connect yourself to the student server `name_student-centos-{n - 1}` and checkout the code from the Automation Bootcamp as described before.

Execute your first_playbook.yaml

```
mkdir automation
cd automation

ansible-playbook -i "localhost," -c local first_playbook.yaml 
```

Some examples are only ansible related and don't do anything on you local system. In some playbook you will do some installation tasks on your system. We have added the manual installation steps that you know what happens in the playbook.

1. second_playbook.yaml

Install a webserver and firewall.
```
#sudo dnf install -y httpd firewalld
```
Register & start the webserver and Firewall.
```
#sudo systemctl enable httpd
#sudo systemctl start httpd
#sudo systemctl enable firewalld
#sudo systemctl start firewalld
```
Create the content we want to show the webserver
```
#echo "Welcome to the example.com intranet!\n"
```
Allow to access the webserver and adjust the firewall rule
```
sudo firewall-cmd --permanent --add-service=http
```

### roles_example

In this section you will find different examples for "real world" projects folder structures and how to use roles. We show how to transform a playbook into a role and how the role will be executed.

Connect yourself to the student server `name_student-centos-{n - 1}` and checkout the code from the Automation Bootcamp as described before.

To execute the playbook use the following example:

Execute your first_role

```
ansible-playbook -i "localhost," -c local first_role 
```

The manual installation steps follows the same approach we have done before. We simply install a webserver.

## Author(s) and Contacts

- [Sebastian Eidner](http://www.acccenture.com/) | [e-mail](mailto:sebastian.eidner@accenture.com)


