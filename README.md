# Summary

This repository contains two Ansible demos automating Cisco ACI that were presented during the **Datacenter Automation Days** webinars in AMER. 

# Demos
### Demo 1
Extremely basic Ansible playbook automating deployment of a basic 3-tier web application on Cisco ACI. No variables, flow control, etc.

### Demo 2
Same ACI configuration as Demo 1 but showcases variables, anchors, flow control, etc.  

# Instructions
These playbooks have been tested with Ansible version 2.13.3 and Cisco ACI collection version 2.2.0
```
$ ansible-galaxy collection install cisco.aci
```

Cisco ACI ansible collection can be upgraded using either --force option or --upgrade option (available in 2.10+):

```
$ ansible-galaxy collection install cisco.aci --force
```

To run the playbooks:
```
$ ansible-playbook -i inventory demoXX/demoXX.yaml
```

To undeploy configuration:
```
$ ansible-playbook -i inventory demoXX/cleanup.yaml
```

