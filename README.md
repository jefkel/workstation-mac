# Workstation configuration playbooks for mac

What: MacOS tools
Why: Reset/Rebuild/update common tools whenever I need to.
How: Ansible Playbook

## From a freshly built Macbook

Open Terminal and install brew via the following:

``` bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Then install Ansible via: `brew install ansible`

## Deploy tools

Setup [Vault/Secrets](VaultPrep.md)

`ansible-playbook setup.yaml`

(OBS needs admin)
---
name, email, sshkey-name
