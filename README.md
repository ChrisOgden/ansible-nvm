markosamuli.nvm
===============

[![Build Status](https://travis-ci.org/markosamuli/ansible-nvm.svg?branch=master)](https://travis-ci.org/markosamuli/ansible-nvm)


Ansible role to install [Node.js](https://nodejs.org/en/) with [NVM](https://github.com/creationix/nvm) on macOS or Ubuntu Developer machine.

It doesn't use [Homebrew](https://brew.sh/) for installing nvm on macOS as it's not a support method by the upstream.

Role Variables
--------------

```yaml
# We're installing stable Node.js version by default
nvm_default_node_version: stable
nvm_node_versions:
  - "{{ nvm_default_node_version }}"

# Initialize shell profile scripts
nvm_init_shell: yes

# Define the shell profile scripts to initialiaze
nvm_shell_profile_scripts:
  - .bashrc
  - .zshrc
```

Example Playbook
----------------

    - hosts: localhost
      connection: local
      roles:
         - { role: markosamuli.nvm }

License
-------

MIT

Author Information
------------------

- [@markosamuli](https://github.com/markosamuli)

