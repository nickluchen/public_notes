<!-- TOC -->

- [1. Synopsis](#1-synopsis)
- [2. Example code](#2-example-code)

<!-- /TOC -->

# 1. Synopsis

```bash
ansible <pattern_goes_here> -m <module_name> -a <arguments>
```

# 2. Example code

```bash
# Perform aptitude update with -K, --ask-become-pass (ask for privilege escalation password)
ansible all -i hosts -a "aptitude update" -b -K

# Perform upgrade with -y
ansible all -i hosts -a "aptitude -y upgrade" -b -K

# SCP files to remote machines
ansible atlanta -m copy -a "src=/etc/hosts dest=/tmp/hosts"
```