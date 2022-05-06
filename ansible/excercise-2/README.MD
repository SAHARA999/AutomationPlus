### Excersie-2

Question: 

Create a task that shows following message: "ansible is awesome"


Answer: 

First create a directory
```
mkdir ansible-files
cd ansible-files

```
Add a file called apache.yml
```
touch first_playbook.yml
```
Afterwards you can start editing your playbook
```
vi first_playbook.yml
```
set up your Playbook as follow:
```
---
- name: variable playbook test
  hosts: localhost
  vars:
     var_one: awesome
     var_two: ansible is
     var_three: "{{ var_two }} {{ var_one }}"
  tasks:
  - name: print out var_three
    debug:
       msg: "{{var_three}}"
````

Save the playbook and head over to code-server terminal and run:

```
ansible-playbook -i "localhost," -c local first_playbook.yaml 
```
