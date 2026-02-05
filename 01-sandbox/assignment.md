---
slug: sandbox
id: 9wn0beriyhpe
type: challenge
title: Sandbox
tabs:
- id: vuxqt46hwyd0
  title: Bastion
  type: terminal
  hostname: bastion
  workdir: /opt/ansible
- id: vxpybzvotomn
  title: Ansible Gateway
  type: website
  url: https://gateway.${_SANDBOX_ID}.instruqt.io
  new_window: true
difficulty: basic
enhanced_loading: null
---

Red Hat Ansible Automation Platform Sandbox
===========================================

This Sandbox environment consists of the following services:

| Host | Service Description |
| -------- | -------- |
| bastion     |  Bastion Host. Installation of the AAP and host interaction can be undertaken from here.     |
| gateway |  The platform gateway is the service that handles authentication and authorization for Ansible Automation Platform. It provides a single entry into the platform and serves the platform’s user interface. |
| controller     |  The platform controller processes events and runs cluster jobs including project updates and cleanup jobs.   |
| hub     |  Automation hub allows you to discover and use new certified automation content from Red Hat Ansible and Certified Partners.  |
| eda     | The Event-Driven Ansible controller is a single-node system capable of handling a variable number of long-running processes (such as rulebook activations) on-demand, depending on the number of CPU cores. |
| postgres     |  The database host for other services in the environment   |

The password for all the services deployed here is the same as the value in the `$_SANDBOX_ID` environment variable.

```bash,run
echo $_SANDBOX_ID
```

All relevant urls can be acquired by running this command.
```bash,run
echo https://gateway.${_SANDBOX_ID}.instruqt.io

echo username: admin
echo password: ${_SANDBOX_ID}
```