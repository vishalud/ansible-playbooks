
oracle-java for Ansible
============




## Summary


This Ansible role has the following features for Oracle JDK:

 - Install JDK 7 or 8 version.
 - Install for CentOS and Debian/Ubuntu families.



## Role Variables

### Mandatory variables

None.

### Optional variables


User-configurable defaults:

```yaml
# which version?
java_version: 8

# which directory to put the download file (for CentOS families)?
jdk_download_path: /tmp
```

For other configurable internals, read `defaults/main.yml` file.


## Usage


### Step 1: add role

Add role name `ansible-oracle-java` to your playbook file.


### Step 2: add variables

Set vars in your playbook file.

Simple example:

```yaml
---
# file: simple-playbook.yml

- hosts: all

  roles:
    - ansible-oracle-java

  vars:
    java_version: 8
```



## Dependencies

None.

