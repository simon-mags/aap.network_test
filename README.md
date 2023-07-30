Network and Connectivity Test Ansible Role
=============================

This Ansible role performs connectivity tests between the Ansible execution environment and remote hosts in the inventory.

**Tasks:**
- Ping test to check if hosts are reachable.
- DNS lookup to resolve the hostname of each host in the inventory.
- Trace route from the Ansible execution environment to each host in the inventory.

**How to use:**
1. Ensure Ansible is installed on the execution environment.
2. Add your hosts to the Ansible inventory file (e.g., `inventory.yml`).
3. Include this role in your playbook and run the playbook to perform the connectivity tests.

**Assumptions:**
- The Ansible execution environment can reach the remote hosts over the network.
- Remote hosts have DNS properly configured to allow DNS lookup.

**Example Playbook:**
```yaml
- hosts: all
  roles:
    - aap.network_test
