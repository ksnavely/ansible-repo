# Provisioning

This brief guide will serve as notes and work towards an actual provisioning script or ansible setup.
For the moment, we choose the paradigm of running ansible playbooks locally on the machine to be used.


## Acquire Hardware

Acquire a machine online somewhere. They only thing you will need is ssh access.

E.g. AWS Ubuntu 14.04.


## Bootstrap the system for ansible and the site

After fetching the box, these few steps should prepare the machine to run the web stack.
 - set up the host in either the production or the staging file

## Run playbook

Once the ansible host file is configured we can run a playbook like so:
```
ansible-playbook --user ubuntu --private-key PATH_TO_KEY -i staging website.yml -v --vault-password-file=PATH_TO_VAULT_PASS_FILE
```
