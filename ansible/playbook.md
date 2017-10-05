# Accessing variables accross hosts

Normally we just use the registered variables across the playbook

```
---
- hosts: localhost
  connection: local
  gather_facts: false

  tasks:
  - name: Spawn Ec2
    ec2:
      image: ubuntu
      instance_type: t1.micro
    register: ec2


- name: Provision App
  hosts: "{{ ec2.instances[0] }}"

  tasks:
  - name: Checkout Tag
    shell: git checkout {{ git_tag }}
...
```

Instead we can access the variable through `hostvars`

```
---
- hosts: localhost
  connection: local
  gather_facts: false

  tasks:
  - name: Spawn Ec2
    ec2:
      image: ubuntu
      instance_type: t1.micro
    register: ec2


- name: Provision App
  hosts: "{{ hostvars['localhost']['ec2']['insatnces'] }}"

  tasks:
  - name: Checkout Tag
    shell: git checkout {{ git_tag }}
...
```
