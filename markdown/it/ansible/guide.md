Example code

```bash
# Perform aptitude update with -K, --ask-become-pass (ask for privilege escalation password)
ansible all -i hosts -a "aptitude update" -b -K

# Perform upgrade with -y
ansible all -i hosts -a "aptitude -y upgrade" -b -K

# SCP files to remote machines
ansible atlanta -m copy -a "src=/etc/hosts dest=/tmp/hosts"
```