Install Datto agent
=========

Anisble role to install Datto backup agent on Linux

Requirements
------------

Must have a Datto device on the network to connect agent deployed.

Role Variables
--------------

`\defaults\main.yml`
```
datto_agent_url: "https://cpkg.datto.com/getLinuxAgent.txt"
datto_apt_keyserver: "keyserver.ubuntu.com"
datto_apt_key: "370C85D709D26407"
datto_apt_repo: "deb [arch=amd64] https://cpkg.datto.com/datto-deb/public/{{ansible_distribution_release}} {{ansible_distribution_release}} main"
```
```
OS family specific variables are loaded to install the correct version of the kernel-headers
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible-role-installdattoagent

